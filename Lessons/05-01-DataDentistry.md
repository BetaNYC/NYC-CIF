> This is from [@namessanti's presentation to the Manhattan Borough President's Office](https://gist.github.com/namessanti/988bed052bd10b054d06)

## CartoDB Workshop: Mapping for Manhattan

About Santiago:

santiago@cartodb.com

@namessanti


### Intro To CartoDB

If you're new to CartoDB, **making an account is easy.** Just click [THIS LINK](https://cartodb.com/signup?plan=academy) and follow the instructions. These accounts are a level-up from our standard free accounts because we <3 you!

#### Welcome to your CartoDB Dashboard!

**The Dasboard** is like the command center for managing your datasets, maps, and account.

![Dashboard](http://i62.tinypic.com/bgr9et.png)

The blue bar on top allows you to:
* Navigate between your maps and datasets
  * Datasets are the backbone of your map visualization. It is important to note that by switching to the **datasets view**, you can work with the data stored on the CartoDB database directly.
* Visit our [CartoDB gallery](https://cartodb.com/gallery/)
* Learn new skills on our [documentation page](http://docs.cartodb.com/).


By clicking the icon on the far right you can:
* Manage your **account settings**
* Visit your **public profile**
* View your **API key**
  * Which will be important for using our APIs and some external tools such as OGR.

![image](http://i61.tinypic.com/16mnbt.png)

### Time to make our first map!

Let's begin by clicking the **green New Map button**. Then choosing to **Make a map from scratch** in the popup.

![button](http://i60.tinypic.com/242ty7k.png)

There are many ways to bring data into CartoDB.

![import](http://i62.tinypic.com/dvhue.png)

From this area you can choose to:
* Create an empty map with no data
* Browse our ever growing **data library**
* Make a map with datasets you have already brought into CartoDB, or
* **Connect a new dataset**.
  * This allows you to choose files from your computer, URL, or one of our connectors such as Twitter.

Keep in mind that you can also **drag and drop** datasets onto your dashboard at anytime and let CartoDB take care of the rest!

####Today we're going to be looking at rat sightings in NYC.

Let's begin by bringing in the **rat sightings 311 data for August 2015** by **command-clicking (or right clicking)** on [THIS LINK](https://data.cityofnewyork.us/api/views/g9n7-nmb7/rows.csv?accessType=DOWNLOAD) and selecting to "Copy Link Address".

* Using a URL allows you to skip bringing data onto your computer as well as allowing users with certain plans to create **automatically syncing and real-time** maps

### The CartoDB Editor

![editor](https://raw.githubusercontent.com/auremoser/nicar-test/master/img/int-viz.jpg)

The CartoDB editor makes it easy to style your map, and run analysis or query your data.

#### The Style Wizard

![style](https://raw.githubusercontent.com/auremoser/nicar-test/master/img/0-wizard.png)

THe Style Wizard allows you to easily tap into CartoDB's Map design language **CartoCSS**.

The basic Syntax is:

```css
selector {
  property: value;
}
```
```css
Map {
  marker-fill: #ffcc00;
}
```

* Changes you make in the wizard change the CartoCSS.
* By working with the CartoCSS directly, the styling possibilities are endless!
* Let's explore some **conditional syling**

![cartocss](http://i59.tinypic.com/2q238qp.png)

####SQL in CartoDB

The cartoDB platform is built on the super-powerful PostgreSQL and PostGIS which make it an incredibly robust tool for working with spatial data!

In the editor itself, it's easy to filter your data sets by using the built in SQL API.

Similar to the Styling Wizard, the 'filters' tab allows you to run queries against your datasets easily, while also making changes to lines of code in the 'SQL' tab.

![filters](http://i58.tinypic.com/nybwk0.png)

Once you run an SQL statement, CartoDB allows you to to create a new dataset from your selection.

![new table](http://i57.tinypic.com/2h3bl7b.png)

### Fun with SQL!

Lets dive a bit more into SQL so we can better understand what's possible.

###Querying data

Try:

```sql
SELECT * FROM rat_aug_2015 
WHERE 
  borough = 'MANHATTAN' 
AND 
  location_type = '3+ Family Apt. Building'
```
Now...

```sql
SELECT * FROM rat_aug_2015
 WHERE 
  ST_DWithin(the_geom, CDB_LatLng(40.7130129, -74.0035165), 500, true)
  ```
  
  or...
  
  ```sql
  SELECT *, 
 ST_Distance(the_geom, CDB_LatLng(40.7130129, -74.0035165)) d 
FROM rat_aug_2015
LIMIT 100
```
**PHEW!**

####Counting points in polygons

Let's bring in a new layer to make more sense of our rat sightings. Click the 'Add Layer' tab in the editor.

![add layer](http://i57.tinypic.com/2e2jb86.png)

In the popup window select 'Data file' and, same as before, **Command-click (or right click)** [THIS LINK](https://github.com/namessanti/workshop-data/blob/master/city_council_districts.zip?raw=true) and select "Copy Link Address" then paste the link into the import popup. This will bring in city council districts for NYC.

![import](http://i57.tinypic.com/3304fhl.png)

we should see our boundary polygons over our rat sighting points. Let's move the polygon data under the point data by dragging and dropping the layer so that the Active Fires layer is on top.

**Congratulations on making your first multi-layered map!**

What we want to do now is count the rat sightings for each boundary to determine which areas have had higher concentrations of rat reports.

Let's add an extra column called 'p_count' to our polygon dataset. We're going to populate this with instances of rats from our point data.

Copy and paste this SQL statement into your editor:
```sql
UPDATE community_districts SET p_count = (SELECT count(*) 
FROM rat_aug_2015 
WHERE ST_Intersects(rat_aug_2015.the_geom, community_districts.the_geom))
```

Going back to our Wizard, we can now make a Choropleth map of fire instances in the various zones.

###But...
Maps have a tendency to distort the truth. Which is why we need to normalize our data by area in order to make a more accurate map. Back in the SQL tab copy and paste this statement:

```sql
SELECT the_geom, the_geom_webmercator, cartodb_id, p_count,
    (p_count / (ST_Area(the_geom::geography)/100000000))
    as n_count
    FROM community_districts
```
This time we're creating a new column named 'n_count' and running a simple mathmatical function to determine number of rats by area, and attribute that to the polygons.

Let's style our map in the Wizard and see our new found accuracy shine!

####Publishing maps

* Title & Metadata
* Adding elements
* Web vs. Mobile view
* Annotations
* Infowindows & legends
* The publish button

### Resources

<ol>
  <li><a href="http://academy.cartodb.com">Map Academy</a>
    <ul>
      <li><a href="http://academy.cartodb.com/courses/01-beginners-course.html">Beginner</a></li>
      <li><a href="http://academy.cartodb.com/courses/02-design-for-beginners.html">Map design</a></li>
      <li><a href="http://academy.cartodb.com/courses/03-cartodbjs-ground-up/lesson-3.html">CartoDB.js</a> – build a web app to visualize your data, allowing for more user interaction</li>
      <li><a href="http://academy.cartodb.com/courses/04-sql-postgis.html">SQL and PostGIS</a> – slice and dice your geospatial data</li>
    </ul>
  </li>
  <li><a href="http://docs.cartodb.com/tutorials.html">CartoDB Tutorials</a></li>
  <li><a href="http://docs.cartodb.com/cartodb-editor.html">CartoDB Editor Documentation</a></li>
  <li><a href="http://docs.cartodb.com/cartodb-platform.html">CartoDB APIs</a></li>
  <li><a href="http://gis.stackexchange.com/questions/tagged/cartodb">Community help on StackExchange</a></li>
  <li><a href="http://cartodb.com/gallery/">CartoDB Map Gallery</a></li>
</ol>


### That's all! Don't forget to share your work and don't hesitate to email me with questions at <santiago@cartodb.com>!
#Thank You!

## References go here

- CartoDB 102 ([CartoDB Academy](http://academy.cartodb.com))
