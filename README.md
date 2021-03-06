# Galway Parks API
## Data Representation and Querying Project 2015
### 3rd year Data Representation and Querying assignment - API Documentation

## Introduction    
This project provides the design and documentation for the dataset "Parks in Galway" which is available at [Data.gov.ie](http://data.gov.ie). This API will be tailored to the front end user that want to check the location, opening/closing hours and facilities of parks local to Galway city and county. Furthermore it will be tailored to the Galway city County Council for adding, deleting and updating park information throughout Galway city and County.

## About the data
This dataset was received in CSV format, and was downloaded from [*Data.gov.ie*](https://data.gov.ie/dataset/parks-in-galway-city).
The CSV file contains 29 rows that can be added to or removed from, the first being a header row with the names of each field. It contains 9 column. Below is a list of all the field names and associated values. No value can be left **NULL** and must contain the correct **Data Types**.

## Table Field-Values

Field | Value | Field | Value
------|---------|---------|-----------
**OBJECTID** | Unique Id (Number) | **DESCR** | Parks description (Text)
**NUMBER** | Unique Number (Number) | **Lat** | Parks latitude (Number)
**NAME** | Parks name (Text) | **Long** | Parks longitude (Number)
**LOCATION** | Parks location (Text) | **EastITM** | International Mapping (Number)
**AREAOFCITY** | Park geo area (Text) | **NorthITM** | International Mapping (Number)
**OPENINGHRs** | Opening hours (Number) | **EastIG** | Mapping (Number)
**FACILITIES** | Parks facilities (Text) | **EastIG** | Mapping (Number)

## Uniform Resource Locator     
<http://galway.ie/parks/25647>   

Url | Component | Url | Component
-----------|----------|----------|-----------        
**http** | Protocol | **galway.ie** | Domain     
**80** | Port | **parks** | Path     
**www** | Subdomain | **25647** | Parameter       
  
## HTTP/1.1 Methods  
Method | Definitions
--------|--------------------------------
**GET** | Retrieve information from the server  
**HEAD** | Retrieve response header   
**POST** | Send data to the server       
**PUT** | Set the data at the URI to the request data   
**DELETE** | Delete the data at the URI

## Status Code Definitions
Code | Definition | Code | Definition     
------|--------|--------|----------      
**200** | Ok | **202** | Accepted    
**400** | Bad Request | **404** | Not Found    
**405** | Method Not Allowed | **503** | Service Unavaiable   


### Querying the Dataset.  
The dataset can be queried using the HTTP/1.1 methods and the URL. The HTTP/1.1 will only receive and send in JSON format. Below is an example of a HTTP/1.1 response where the JSON object containing the park name that the HTTP/1.1 method was querying.<http://galway.ie/parks/[Name]>  
Where you replace [Name] with the Name.  
<http://galway.ie/parks/ShantallaPark> 

<!--HTTP/1.1 is just to illustrate language - has no formatting use in markdown other than block of its own-->      
```HTTP/1.1     
GET http://galway.ie/parks/ShantallaPark  
```    
### HTTP Response JSON     
```json   
[ {...} {      
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
        }, {...} ]   
  ```
  
# Admin Users
The admin user will need to query, update and delete from the dataset using the HTTP methods and URL. 

**Create the admin user**

URI | Method    
----|-------    
admin | POST    
```json
{
   "name" : "my_username",
   "first-name" : "First",
   "last-name" : "Last",
   "display-name" : "First Last",
   "email" : "admin@example.com",
   "password" : {
      "value" : "my_password"
   },
   "active" : true
}
```
**Setting admin password**

URI | Method    
----|-------    
admin/password?username=USERNAME | POST   
```json
{
   "value" : "new_password"
}
```


## HTTP Request by admin using GET method 
<!--HTTP/1.1 is just to illustrate language - has no formatting use in markdown other than block of its own-->      
```HTTP/1.1    
GET http://admin/password@galway.ie/parks/25647 
```   
#### HTTP Response JSON    
```json   
  [ {...} {      
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
          }, {...} ]       
  ```
  
## HTTP Request by admin using POST method 
<!--HTTP/1.1 is just to illustrate language - has no formatting use in markdown other than block of its own-->      
```HTTP/1.1    
POST http://admin/password@galway.ie/parks/25647/?OPENINGHRs=Closed 
```   
#### HTTP POST JSON    
```json   
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
#### HTTP Response  
```json
ok:true
```
```json   
  [{      
    "OBJECTID":"25647",   
    "NUMBER":"1",   
    "NAME":"Corrib Park",   
    "LOCATION":"Newcastle, Galway",   
    "AREAOFCITY":"City- West",   
    "OPENINGHRs":"Closed",   
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
  
## HTTP Requst by admin using PUT method 
<!--HTTP/1.1 is just to illustrate language - has no formatting use in markdown other than block of its own-->    
```HTTP/1.1     
PUT http://admin/password@galway.ie/parks -H "Content-Type: application/json" -d @clareCountyParks.json 
```     
#### HTTP PUT clareCountyParks.json
```json   
[ 
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
  {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...} {...}
]       
  ```
  
## HTTP Request by admin using DELETE method 
<!--HTTP/1.1 is just to illustrate language - has no formatting use in markdown other than block of its own-->     
```HTTP/1.1       
DELETE http://admin/password@galway.ie/parks/clareCountyParks.json 
```    
#### HTTP Response
```json   
ok:true      
  ```
