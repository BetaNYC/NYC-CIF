# Week 6 - Crushing the data

# Getting to know a Community District's data

## Objectives 

For the next few weeks, you will be working on understanding NYC 311 data. This exercise requires you to use Socrata, Microsoft Excel or Google Sheets, and CartoDB. Your task is to make graphs and maps of the following data. This is due on the week of Nov 9. 

To complete this task, create a google doc, answer this questions, and share it with 'cif@beta.nyc'.

Tips located at the bottom of this email.

## Data to explore

### **NYC 311 Service Requests over seasons**

 - Outline 5 assumptions about NYC 311 data. Try to make one assumption per season. Write them down.
 - Make a graph comparing seasons over the following years (2012, 2013, 2014, 2015). Use traditional definitions of [meteorological seasons](http://www.timeanddate.com/calendar/aboutseasons.html).
  - Fall 2012, 2013, 2014, 2015
  - Winter 2012 (include 2011 data), 2013, 2014
  - Spring 2012, 2013, 2014, 2015
  - Summer 2012, 2013, 2014, 2015
 - What are the top 10 complaints per season. Make a table that lists seasons, year, service request, and count. Put this into a google sheets
 - Have your assumptions changed? If so, how? Write them down.


 - Diving into winter 2014 & 2015 data.
   -- What are the differences between the two seasons?
   -- What might be 2016's top 10 issues?
	 -- **Note on this: Winter 2015 is the months of Nov 2014-Feb 2015. You should be comparing the 2015 season to the previous year (Nov 13-Feb 14), and then making predictions for this upcoming Winter (2016).**


### **Heat and Hot Water Service Requests**

 - Make a pivot table of "Heat and Hot Water" service requests per month (2012, 2013, 2014, 2015) per issue description. See (img/exersize3-piviot-table.jpg) for how to set up this pivot table.
 - What are the months have the most "Heat and Hot Water" service requests.
 - Why might these months have more service request?
 - Over the years, are any of these service complaints, repeat callers? If so, what are the address? Go to google street view and take a photo of these locations. Search google news and see if there are any articles about these address. (Note, you will have to map out these per descriptions via CartoDB.)
 
**Note!**
 - On Socrata, you will have to make a few filters and combine them in Excel. Please use [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=0) to ensure proper spelling. 
	 - Complaint Type is "non-residential heat"
	 - Complaint Type is "heat/hot water"
	 - Complaint Type is "heating"
	 - Complaint Type is "school maintenance" with descriptor "heating problem"


### **Rodent Service Requests**

 - Make a pivot table of rodent requests per month (2012, 2013, 2014, 2015) per issue description. See (img/exersize3-piviot-table.jpg) for how to set up this pivot table.
 - Which months have the most rodent service requests? Why might this be the case?
 - Collectively, is there a part of the community district that has an overwhelming rodent problem? If so, does google street view show you anything? (Note, you will have to map out these per descriptions via CartoDB.)
 - Looking at all service requests, is there an area you would target to increase 311 service requests?

**Note!**
 - On Socrata, you will have to make a few filters and combine them in Excel. Please use [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=0) to ensure proper spelling. 
 - For this task, you will have to create two separate filters.
	 - First, Complaint Type contains "rodent"
	 - Second, Descriptor contains "rodent"
	 - Third, Descriptor contains "vermin"

### **Street condition / pothole**

 - Make a pivot table of the various street condition complaints per month (2012, 2013, 2014, 2015) per description. See (img/exersize3-piviot-table.jpg) for how to set up this pivot table.
 - What are your Community District street condition descriptors?
 - What are the top five street condition issues per year?
 - Create a "realtime" 60 day map of street conditions. (Note, you will have to make this map via CartoDB.)
 - Looking at seasonal street conditions, what can you tell? Is there a particular street condition that appears at a particular time of the year? If so, what is it?

**Note!**
 - On Socrata, you will have to make a few filters and combine them in Excel. Please use [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=0) to ensure proper spelling. 
 - For this task, you will have to create several filters.
  - Descriptor contains "general bad condition"
  - Descriptor contains "Pothole"
  - Descriptor contains "hummock"
  - Descriptor contains "bad condition"
  - Descriptor contains "rough, pitted or cracked roads"
  - Descriptor contains "failed street repair"
  - Descriptor contains "cave-in"

### **Noise**

 - Make a pivot table of the various noise complaints per month (2012, 2013, 2014, 2015) per description. See (img/exersize3-piviot-table.jpg) for how to set up this pivot table.
 - In this chart, outline the top 10 cells. 
 - Which quarters have the most noise service requests? Why might this be the case?
 - Where are Community District noise hot spots? (Note, you will have to map out these per descriptions via CartoDB.)
 - Is there consistency year over year? If so, document them in a google doc with Google street view photos.

**Note!**
 - On Socrata, you will have to make a few filters and combine them in Excel. Please use [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=0) to ensure proper spelling. 
 - For this task, you will have to create one filter.
	 - Complaint type contains "noise"

### **Illegal parking / blocked driveway**

 - Make a pivot table of the various illegal parking & blocked driveway complaints per month (2012, 2013, 2014, 2015) per description. See (img/exersize3-piviot-table.jpg) for how to set up this pivot table.
 - Which months have the most illegal parking & blocked driveway service requests? Why might this be the case?
 - Where are Community District illegal parking & blocked driveway hot spots? You will have to use CartoDB to complete this task.
 - Is there consistency year over year? If so, document them in a google doc with Google street view photos.

**Note!**
 - On Socrata, you will have to make a few filters and combine them in Excel. Please use [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=1896934307) to ensure proper spelling. 
 - For this task, you will have to create one filter.
	 - Descriptor contains "blocked hydrant"
	 - Descriptor contains "blocked sidewalk"
	 - Descriptor contains "double parked"
	 - Descriptor contains "commercial overnight"
	 - Complaint Type contains "blocked driveway"

---
Tips on completing the assignment:

1. To complete the seasonal research, you will need to create a filter, select your community district, and then build a date filter between a set of dates. You will have to make a filter per season. Remember to save each filter.

2. To include all events between two days, lets say 1 June to 30 Aug, you will need to select 1 June, 12:00 AM till 30 Aug, 12:00 AM. 

3. When making a pivot table in Excel, you'll want to select "complaint type" and "descriptor" as rows. Then, you'll want to "count" the "unique keys." This will give you a count of every incident type.

4. **You will need to use the following documents to search for relevant Complaint Type and Descriptors.**

 * [NYC 311 Complaint Types - "Socrata Roll up as a google doc"](https://docs.google.com/spreadsheets/d/1Vvwlyy0mmALpG1JH04wZHes6pNzxiG_-WT4BtyfD5m0/edit#gid=0)
 * [NYC 311 Complaint Types and descriptors](https://data.cityofnewyork.us/Social-Services/NYC-311-Complaint-Type-Descriptor-Count/h9an-u3fn) this is a live view and might need to be exported.


---
## Notes on exporting data from Socrata to CartoDb

**Building a data universe** 
 * open up socrata
 * open up 311 data
 * create a universe of the data
 * first select your community board
 * select “created date” “is after” 01/01/2012
 * then add “complaint type” “contains” Noise (or whichever type you want)
 * Important! This is where you want to export data for cartoDB. Go to “export” and download the CSV to upload to CartoDB. Once you have saved the raw data, you can move on to the roll up portion.

**Roll up within Socrata**
* now go to sort and roll-up
* uncheck sort
* check roll-up
* group by “created date” based on “month”
* add two more group by’s
 - make the first “complaint type” 
 - make the second “descriptor”
 - then change roll-up “unique key” and function “count”
* This should organize data in a table with columns for "complaint type", "descriptor", and a count of unique ids. Each row should be a month.
* export using CSV for excel 

**Pivot Table in Excel / Google Docs**
* open downloaded file in Excel
* select the data universe 
* create a pivot table 
* the pivot table builder
- in columns should be “created date”
- in row labels should be “complaint type” and “descriptor”
- in values should be “unique key”
