# Intro to NYC's Open Data

## Open Data & Mapping Objectives

Learn rigorous, professional methods for working with open data and large datasets. This 5-hour workshop provides an intensive overview of data acquisition and assessment techniques. You will learn what questions to ask when acquiring data, how to obtain a wide variety of datasets, and how to think critically about data quality. By the end of the workshop you will have a firm grounding in how to apply these techniques in visual analysis outputs and web maps.

Topics Include: Working with large datasets, evaluating data quality and accuracy, and documenting data sources and methods, open data sources, acquiring data.


## Suggested readings

* Watch [Ben Wellington’s TedX talk](https://www.youtube.com/watch?v=6BTg8OXhEZk#t=11)
* Review [NYC 311 Map](http://www1.nyc.gov/apps/311srmap/)
* See how [Manhattan Community Board 6 uses NYC 311 data](http://cbsix.org/resources/mapping-311-requests-cb6/).


## Open Data Workshop Day

### Introductions


**What is open data**?

Open Data is the idea that certain data should be freely available to everyone to use and republish as they wish, without restrictions from copyright, patents or other mechanisms of control. The goals of the open data movement are similar to those of other "Open" movements such as open source, open hardware, open content, and open access.
http://en.wikipedia.org/wiki/Open_data

**Why do we fight for it?**

Civic hacking mindset
Civic Hacking is using technology and design to make where we live better. http://www.codeforamerica.org/blog/2013/06/07/defining-civic-hacking/

Civic Hacker - One who collaborates with others to create, build, and invent open source solutions using publicly-released data, code and technology to solve challenges relevant to their neighborhood, city, state, or country. http://en.wiktionary.org/wiki/civic_hacker




### Setting expectations

**Day’s Objective**

Build a map using NYC 311 data that tells a story, and discuss the potential biases across data collection, mapping, and cultural assumptions.

**Tools for the day**

* [Socrata](http://www.socrata.com/) (as a company and software platform)
* [CartoDB](http://cartodb.com/)
* [NYC Data Portal](http://nyc.gov/data)
* NYC 311 Data - [link](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9?)
* BetaNYC Community Board Boundaries - ([link](http://data.beta.nyc/dataset/nyc-community-districts))
* Listing of NYC 311 Complaint Types from the NYC 311 Map ([link to google doc](https://docs.google.com/document/d/1EhQm2PUcMF-tC8JLH-O52ILU-oj9RMHzfwfoFxgnT7M/edit?usp=sharing))


**Types of thematic maps**

* [Choropleth map](http://en.wikipedia.org/wiki/Choropleth_map) (this will be our focus)
* [Heat maps](http://en.wikipedia.org/wiki/Heat_map)
* [dot or density maps](http://en.wikipedia.org/wiki/Dot_distribution_map)
Note: [IndieMapper](http://indiemapper.com/app/learnmore/) has good blog posts describing the types of map (ie. [choropleth](http://indiemapper.com/app/learnmore.php?l=choropleth), [proportional symbol](http://indiemapper.com/app/learnmore.php?l=proportional_symbols), and [dot density](http://indiemapper.com/app/learnmore.php?l=dot_density))

**Storytelling of critical considerations / bias**

* data collection
* mapping
* cultural
* how to tell [data stories](https://www.youtube.com/watch?v=6xsvGYIxJok)


### Tools Demonstration

Note - This lecture will take the form of a live demonstration (kind of like a cooking show) - instructors will go through the steps of acquiring, processing, and putting data on a map.

* Finding data - overview of NYC’s open data portal and Census Reporter.
* Processing tools - an overview of Socrata’s built in data processing tools.
* Visualization tools - an overview of Socrata’s built in mapping tools and basic overview of CartoDB.

### Storytelling of critical considerations / bias

* Note - This discussion will outline critical considerations to note and an open discussion on data bias.
* Considerations to review: data collection, mapping, and cultural considerations.


## Resources

### Data Tools

* NYC.gov has a short list of datasets available. This is a [dataset of datasets](https://data.cityofnewyork.us/dataset/NYC-Open-Data-Available-Datasets/j9m9-eu6n).
* [NYC.gov’s developer portal](http://developer.cityofnewyork.us)
* [BetaNYC’s NYC Open Data Resource collection](https://docs.google.com/a/betanyc.us/spreadsheets/d/1R7O_FZLNB8VV5eoPDNATb-f0njjUsJwmz22cT_OB3fw/edit#gid=0) - this is a broad collection of open data resources for the New York City Metropolitan area. This list focuses on New York City. If you would like to add more, please feel free to do so.


### Data Transformation Tools

* [Open Refine](http://openrefine.org) is a “powerful tool for working with messy data.” Some YouTube videos about open refine ([Video 1](https://www.youtube.com/watch?v=B70J_H_zAWM) - [Video 2](https://www.youtube.com/watch?v=cO8NVCs_Ba0) - [Video 3](https://www.youtube.com/watch?v=5tsyz3ibYzk)).
* [ETL for America](https://github.com/codeforamerica/etl-for-america/wiki) - List of resources for data transformation
* [Kimono](http://kimonolabs.com)
* [ScraperWiki](https://scraperwiki.com)
* [Import.io](https://import.io/advanced-data-platform)

**Geocoding**

- How to [geocode address](https://github.com/talos/nyc-geoclient) in NYC (requires knowledge of Python)
- Here’s an example of [how to geocode using google docs](https://www.mapbox.com/blog/mapping-google-doc-spreadsheet/). 


### Map Making Tools

- [CartoDB](http://cartodb.com/)
- [Google Fusion Tables and Maps](https://support.google.com/fusiontables/answer/2571232) - (Note, you will need a google account for this.)
- [Open Source GIS software](http://en.wikipedia.org/wiki/List_of_geographic_information_systems_softwarehttp://en.wikipedia.org/wiki/List_of_geographic_information_systems_software)
- [MapBox](https://www.mapbox.com)
- [TileMill](https://www.mapbox.com/tilemill/)


### Introduction to Cartography

- What are choropleth maps? ([link](http://en.wikipedia.org/wiki/Choropleth_map) and [link](http://indiemapper.com/app/learnmore.php?l=choropleth))
- Duke University’s [Introduction to Data Visualization](http://guides.library.duke.edu/datavis)
- [IndieMapper’s Mapmaking Guide](http://indiemapper.com/app/learnmore/)

**How to cite data and maps**

- At a minimum, agency / source and date. If you are using US Census data, list the table that the data came from (for example, 2010 U.S. Census or 2009-2013 American Community Survey).
- [Perma](https://perma.cc/) - an effort to create permanent url links for citation purposes
- Get data button ([link](https://github.com/BetaNYC/getDataButton)) When building a website, report, map, data visualization, or any other project, use this button to link to the underlying data. That's it! Tell your friends! Let's make this a thing!

### Glossary of Terms
We’ve made [a short list of glossaries](https://docs.google.com/a/betanyc.us/spreadsheets/d/1R7O_FZLNB8VV5eoPDNATb-f0njjUsJwmz22cT_OB3fw/edit#gid=1895864627) that give a good overview of Open Data terms. In class, we will review the highest level of terms.


## Blogs of note

- [I Quant NY](http://iquantny.tumblr.com/)
- [NYC’s Open Data Blog](http://nycopendata.tumblr.com/)
- [School of Data](http://schoolofdata.org/)
- [Socrata’s Open Data Blog](http://www.socrata.com/blog/)

