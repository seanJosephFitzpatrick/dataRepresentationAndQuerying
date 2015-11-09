# Galway Parks API
## Data Representation and Querying Project 2015
###Sean Fitzpatrick

## Introduction    
This project provides the design and documentation for the dataset "Parks in Galway" which is available at [Data.gov.ie](http://data.gov.ie). This API will be tailored to the front end user that want to check the location, opening/closing hours and facilities of parks local to Galway city and county. Futhermore it will be tailored to the Galway city County Council for adding, deleting and updating park information throughout Galway city and County.

## About the data
This dataset was received in CSV format, and was downloaded from [*Data.gov.ie*](https://data.gov.ie/dataset/parks-in-galway-city).
The CSV file contains 29 rows that can be added to or removed from. It contains 9 column.
   - **Dataset Fields**.
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
**OBJECTID** | Unique Id (Number)
**NUMBER** | Unique Number (Number)
**NAME** | Parks name (Text)
**LOCATION** | Parks location (Text)
**AREAOFCITY** | Park geo area (Text)
**OPENINGHRs** | Opening hours (Number)
**FACILITIES** | Parks facilities (Text)
**DESCR** | Parks description (Text)
**Lat** | Parks latitude (Number)
**Long** | Parks longitude (Number)
**EastITM** | International Mapping (Number)
**NorthITM** | International Mapping (Number)
**EastIG** | Mapping (Number)
**EastIG** | Mapping (Number)

##Uniform Resource Locator     
*http://galway.ie/parks/25647/*   

url | Component   
-----------|-----------     
**http** | Protocol   
**80** | Port   
**www** | Subdomain   
**galway.ie** | Domain   
**parks** | Path   
**25647** | Parameter     

**JSON Results by OBJECTID**     
``` json   
  [{      
    "OBJECTID":"25647",   
    "NUMBER":"1",   
    "NAME":"Corrib Park",   
    "LOCATION":"Newcastle, Galway",   
    "AREAOFCITY":"City- West",   
    "OPENINGHRs":"No restricted opening hours",   
    "FACILITIES":"Passive Recreational Walkways, 3G Artificial Surface Pitch, Multi- Use Games Area(MUGA), Planting areas with flowers, sh",   
    "DESCR":"Local Neighbourhood Park",   
    "Lat":"53.279",   
    "Long":"-9.075",   
    "EastITM":"528328.238",   
    "NorthITM":"725961.154",   
    "EastIG":"128361.999",   
    "NorthIG":"225932.124"   
  },]       
  ```


##HTTP Request Methods  
Method | Definitions
--------|--------------------------------
**GET** | Retrieve information from the server  
**HEAD** | Retrieve response header   
**POST** | Send data to the server       
**PUT** | Set the data at the URI to the request data   
**DELETE** | Delete the data at the URI


###Searching for park by name  
*http://galway.ie/parks/[Name]*   
Where [Name] is used to search for park   
*http://galway.ie/parks/[Shantalla/Park]*   

**JSON Results by NAME** 
```json   
[{      
    "OBJECTID":"45826",   
    "NUMBER":"8",   
    "NAME":"Shantalla Park",   
    "LOCATION":"Newcastle, Galway",   
    "AREAOFCITY":"City- West",   
    "OPENINGHRs":"No restricted opening hours",   
    "FACILITIES":"Passive Recreational Walkways, 3G Artificial Surface Pitch, Multi- Use Games Area(MUGA), Planting areas with flowers, sh",   
    "DESCR":"Local Neighbourhood Park",   
    "Lat":"53.279",   
    "Long":"-9.075",   
    "EastITM":"528328.238",   
    "NorthITM":"725961.154",   
    "EastIG":"128361.999",   
    "NorthIG":"225932.124"   
  },]   
  ```

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
  
