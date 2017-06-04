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
### air_quality_model_hkust
  * _id: an object id created by mongodb
  * station_code: string, the id of air quality station, map to air_station_hksut
  * station_name: string, the name of air quality station, map to air_station_hkust
  * CAMx: model name
    - CO
    - O3
    - SO2
    - NOx
    - NO2
    - PM2_5
    - PM10
  * NAQPMS: model name
    - same as CAMx
  * CMAQ: model name
    - same as CAMx

# TBD