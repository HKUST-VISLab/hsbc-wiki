## Database: POI
This database is designed to store POI (Point of interest). This database has following one collection: **POI** 
- traffic_speed 

***
### traffic_speed
This  collection stores the POI data in Hong Kong, the data is collected from OSM (Open Street Map). 
Ref: https://www.openstreetmap.org/
The total number of POIs is 28253. 

###### 607 roads are monitored
  * _id: an object id created by mongodb
  * id: point id in OSM, ref OSM.node
  * category: first level category, the classification can be refered to 
  * category_1: second level category if possible
  * version: OSM version
  * traffic_speed: string, the estimated average traffic speed of the roads(km/h)
  * location: the GPS location of POI [longitude, latitude]
  * tags: individual attributes of this POI
an example

``` javascript
{
    "_id" : ObjectId("5a10aaa465cd561c240f0358"),
    "id" : "24358842",
    "osm_value" : "tram_stop",
    "category" : "public_transport",
    "category_1" : null,
    "version" : "1",
    "location" : [ 
        114.1498742, 
        22.2878152
    ],
    "tags" : {
        "ref" : "19E",
        "name" : "港澳碼頭 Macau Ferry Terminal",
        "tram" : "yes",
        "name:en" : "Macau Ferry Terminal",
        "name:zh" : "港澳碼頭",
        "railway" : "tram_stop",
        "wheelchair" : "no",
        "public_transport" : "stop_position"
    }
}
```
