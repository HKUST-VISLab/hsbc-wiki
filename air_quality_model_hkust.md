## Database: air_quality_model_hkust

- weather_station_hkust
- air_station_hkust
- air_quality_model_hksut
- weather

***
### weather_station_hkust

***
### air_station_hkust

*** 
### collection: air_quality_model_hkust
  * _id: an object id created by mongodb
  * station_code: string, the id of air quality station, map to air_station_hksut
  * station_name: string, the name of air quality station, map to air_station_hkust
  * CO:
    - CAMx: the prediction value of CAMx model
    - NAQPMS: the prediction value of NAQPMS model
    - CMAQ: the prediction value of model
    - obs: the observation value
  * O3
    - same as CO
  * SO2
  * NOx
  * NO2
  * PM2_5
  * PM10

an example
See the example of air quality model
``` json
{
    "_id" : ObjectId("59352ae4fd72e87b131dbb74"),
    "station_code" : "CW_A",
    "time" : "2017-05-01 00:00:00",
    "NO2" : {
        "obs" : "34.36",
        "CAMx" : "34.26",
        "CMAQ" : "27.43",
        "NAQPMS" : "10.11"
    },
    "PM10" : {
         "obs" : "36.40",
         "CAMx" : "28.59",
         "CMAQ" : "36.59",
         "NAQPMS" : "24.76"
    },
    "SO2" : {
        "obs" : "4.39",
        "CAMx" : "6.74",
        "CMAQ" : "4.24",
        "NAQPMS" : "1.81"
    }
}
```

*** 
### collection: weather_model_hkust
  * _id: an object id created by mongodb
  * station_code: string, the id of air quality station, map to air_station_hksut
  * time: string, the name of air quality station, map to air_station_hkust
  * loc: list, the list of location, [longitude, latitude]
  * relative_humidity: Double, the relative humidity value (%)
  * temperature: Double, the temperature value (Degree Celsius)
  * wind_speed: Double, the speed of wind (m/s)
  * wind_direction: Double, the direction of wind (Degree)


an example
See the example of weather model
``` json
{
    "_id" : ObjectId("59576a975281aa717e64517c"),
    "loc" : [ 
        113.9219, 
        22.3094
    ],
    "time" : "2017-05-01 00:00:00",
    "relative_humidity" : 78.0,
    "station_code" : "HKA_AWS",
    "temperature" : 23.5,
    "wind_speed" : 4.1667,
    "wind_direction" : 90.0
}
```

# TBD