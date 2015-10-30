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

##URL's
**Galway County Council**
*http://galway.ie/*
Display Galway County Council home page


**Galway county Parks**
*http://galway.ie/parks/*
Dispaly Galway County Council Parks home page


**Roscam park**
*http://galway.ie/parks/roscam/*
Display Roscam Park information details

- **Location**: Name of townland, town that park resides in
- **Facilities**: List of all facilities available on site
- **Description**: Description of what kind of park, Neighborhood - City park
- **Opening/Closing hours**: List of parks known opening/closing hours
- **Area of the city**: Geographical map of the parks location with in the city
- **Latitude and Longitude**: Latituade and longitude of the park


**Park location**
*http://galway.ie/parks/roscam/location*
Display park location details

**Park facilities**
*http://galway.ie/parks/roscam/facilities*
Display park facilities details

**Park description**
*http://galway.ie/parks/roscam/description*
Display park description details

**Park opening/closing**
*http://galway.ie/parks/roscam/opening/closing*
Display park opening/closing details

**Park areaOfCity**
*http://galway.ie/parks/roscam/areaOfCity*
Display park areaOfCity details

**Park latitude/longitude**
*http://galway.ie/parks/roscam/latitude/longitude*
Display park latitude/longitude details


##JSON
**All requests are sent in JSON format**

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

##API Methods

###Name

- **park.getName** // Retrieves the park name
- **park.setName**: Set the park name
    
###Number

- **park.setNumber**
    
###Location

- **park.getLocation**
- **park.setLocation**
    
###Hours

- **park.getHours**
- **park.setOpen**
- **park.setClose**
    
###Facilities

- **park.getFacilities**
- **park.setFacilities**
    
###Description

- **park.getDescription**
- **park.setDecription**
    
###Latitude

- **park.getLatitude**
- **park.setLatitude**
    
###Longitude

- **park.getLongitude**
- **park.setLongitude**
  
