# Project Title
## Data Representation and Querying Project 2015
###Sean Fitzpatrick

## Introduction
This project provides the design and documentation for the dataset "Parks in Galway" which is available at [Data.gov.ie](http://data.gov.ie). This API will be tailored to the front end user that want to check the location, opening/closing hours and facilities of parks local to Galway city and county. Futhermore it will be tailored to the Galway city County Council for adding, deleting and updating park information throughout Galway city and County.

## About the data
This dataset was received in CSV format, and was downloaded from [*Data.gov.ie*](https://data.gov.ie/dataset/parks-in-galway-city).
The CSV file contains 29 rows that can be added to or removed from. It contains 9 column.
   - **Table classified by attribute**.
    - **ObjectId**: Table attribute unique id.
    - **Number**: Table attribute unique park number.
    - **Name**: Table attributes name of park.
    - **Location**: Table attributes location of each park.
    - **Facilities**: Table attributes the facilities of each park.
    - **Dscription**: Table attributes the description of each park.
    - **Open**: Table attributes the opening hours of each park.
    - **Close**: Table attributes the closing hours of each park.
    - **AreaOfCity**: Table attributes the city area of each park.
    - **Latitude**: Table attributes the latitude of each park.
    - **Longitude**: Table attributes longitude of each park.
    

##Item

Field | Description
------|------------
**ObjectId** | Item Unique Id (Number)
**Number** | Item unique Number (Number)
**Name** | Item park name (Text)
**Location** | Item park location (Text)
**Facilities** | Item park facilities (Text)
**Description** | Item park description (Text)
**Open** | Item opening hours (Number)
**Close** | Item closing hours (Number)
**AreaOfCity** | Item park geo area (Text)
**Latitude** | Item park latitude (Number)
**Longitude** | Item park longitude (Number)

#JSON

[
  {
    "OBJECTID":16,
    "NUMBER":29,
    "NAME":"Roscam Park",
    "LOCATION":"Roscam, Galway",
    "AREAOFCITY":"City- East",
    "OPENINGHRs":"No restricted opening hours",
    "FACILITIES":"Pedestrian Walkways, Playgrounds, Tennis Courts, Basketball Court, 1 Soccer Pitch, 1 5-a-side pitch, Planting areas with",
    "DESCR":"Local Neighbourhood Park",
    "Lat":53.274,
    "Long":-8.994,
  },
]


