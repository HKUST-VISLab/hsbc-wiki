## Database: traffic
This database is designed to store traffic information. This database has following two collections: **traffic_speed** and **traffic_volume** 

- traffic_speed 

***
### traffic_speed
This  collection stores the real time traffic speed data of the main roads in Hong Kong, the data is collected from DATA.GOV.HK, https://data.gov.hk/en-data/dataset/hk-td-tis-traffic-speed-map. The data will be updated every 2 minues. 
Ref: https://data.gov.hk/en-data/dataset/hk-td-tis-traffic-speed-map
Fetch_time is the time to collect all the 607 road from the data.gov.hk, all the fetch time of 607 roads are the same, capture_data the the time generating the speed data, the catpure time of all the 607 records is not exactly the same.

###### 607 roads are monitored
  * _id: an object id created by mongodb
  * link_id: string, unique id for links(--geo_maps.hk_link.id)
  * region: string, to the sixth decimal point
  * road_type: string, the type of road(MAJOR ROUTE – Refers to roads with speed limit of 70km/h or above; URBAN ROAD – Refers to roads with speed limit of 50 km/h )
  * road_saturation_level: To define the traffic condition of the roads. (TRAFFIC GOOD, TRAFFIC AVERAGE, TRAFFICE BAD)
  * traffic_speed: string, the estimated average traffic speed of the roads(km/h)
  * capture_date: time of generating the traffic speed data YYYY-mm-DD HH:MM:SS
  * fetch_time: time when fetch data
an example

``` javascript
{
    "_id" : ObjectId("59145f9bda8f5d922aa337da"),
    "link_id" : "3006-30069",
    "region" : "K",
    "road_saturation_level" : "TRAFFIC AVERAGE",
    "traffic_speed" : "26",
    "capture_date" : "2017-05-29 16:20:35",
    "osm_way_id": "2019929201"
    "fetch_time" : "2017-05-29 16:21:54"
}
```

***
### traffic_volume
This  collection stores the traffic volumn data of the roads in Hong Kong, currently the we get some sample data of from our collaborators (task5). 

###### 607 roads are monitored
  * _id: an object id created by mongodb
  * link_id: string, unique id for links(--geo_maps.hk_link.id)
  * region: string, to the sixth decimal point
  * road_type: string, the type of road(MAJOR ROUTE – Refers to roads with speed limit of 70km/h or above; URBAN ROAD – Refers to roads with speed limit of 50 km/h )
  * traffic_speed: string, the estimated average traffic speed of the roads(km/h)
  * capture_date: time of generating the traffic speed data YYYY-mm-DD HH:MM:SS
  * forecast_time: time of forecast 
  * volume: number of vehicles per hour
an example

``` javascript
{
    "_id" : ObjectId("59145f9bda8f5d922aa337da"),
    "link_id" : "3006-30069",
    "region" : "K",
    "road_saturation_level" : "TRAFFIC AVERAGE",
    "traffic_speed" : "26",
    "capture_date" : "2017-05-29 16:20:35",
    "osm_way_id": "2019938223",
    "forecast_time": null,
    "volume": 27
}
```