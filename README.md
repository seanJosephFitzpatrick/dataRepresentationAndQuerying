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

Field | Value 
------|------------
Field 1 | **ObjectId** | Unique Id (Number)
Field 2 | **Number** | Unique Number (Number)
Field 3 | **Name** | Park name (Text)
Field 4 | **Location** | Park location (Text)
Field 5 | **AreaOfCity** | Park geo area (Text)
Field 6 | **Open** | Opening hours (Number)
Field 7 | **Facilities** | Park facilities (Text)
Field 8 | **Description** | Park description (Text)
Field 9 | **Latitude** | Park latitude (Number)
Field 10 | **Longitude** | Park longitude (Number)
Field 11 | **EastITM** | Mapping (Number)
Field 12 | **NorthITM** | Mapping (Number)
Field 13 | **EastIG** | Mapping (Number)
Field 14 | **EastIG** | Mapping (Number)

##URL's

###Location   
*http://galway.ie/parks/[Location]*   
Where location is replaced with location   
*http://galway.ie/parks/Corrib Park*

###JSON

[  {
    "FIELD1":"1",
    "FIELD2":"1",
    "FIELD3":"Corrib Park",
    "FIELD4":"Newcastle, Galway",
    "FIELD5":"City- West",
    "FIELD6":"No restricted opening hours",
    "FIELD7":"Passive Recreational Walkways, 3G Artificial Surface Pitch, Multi- Use Games Area(MUGA), Planting areas with flowers, sh",
    "FIELD8":"Local Neighbourhood Park",
    "FIELD9":"53.279",
    "FIELD10":"-9.075",
    "FIELD11":"528328.238",
    "FIELD12":"725961.154",
    "FIELD13":"128361.999",
    "FIELD14":"225932.124"
  },]

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
  
