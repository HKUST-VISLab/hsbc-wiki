## Database: hk_AirQuality_prediction

- air_quality_prediction: This includes predicted AQ data based on Current day. The air quality parameters consistently contains the following: PM10, PM2.5, O3, NO2, NOX, SO2.   

***
### air_quality_prediction
  * _id: an object id created by mongodb
  * model: string, by default model = CMAx, CMAQ, or NAQPMS
  * initial_date: string, time in the format of "%Y-%m-%d %H:%M"
  * forecast_days: num
  * region: string, in the format of "lng1, lat1, lng2, lat2", where lng1, lng2, lat1, lat2 are floats, and lng2>lng1, and lat2 > lat1  
  * domain: num (km), by default domain = 1km or 3km
  * number_domain: num, by default number_domain=size of region / domain
  * PM2.5 (one of the Fine suspended particulate): [num (ug/m3),...,num], to the first decimal point,  hourly concentration   
  * PM10 (Respiratory Suspended Particulates): [num (ug/m3),...,num], to the first decimal point,   hourly concentration
  * O3: [num (ppb),...,num], to the first decimal point,  hourly concentration
  * NO2: [num (ppb),...,num], to the first decimal point,  hourly concentration 
  * NOX: [num (ppb),...,num], to the first decimal point,  hourly concentration  
  * SO2: [num (ppb),...,num], to the first decimal point,  hourly concentration
  * WS(Wind Spd): [num (m/s), ..., num], to the first decimal point 
  * WD(Wind Dir): [char (Degree),..., char], "N","NE","E","SE","S","SW","W","NW" 

an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "model": "CMAx", 
>          "initial_date" : "2017-06-27 12:00",
>          "forecast_days" : 1,
>          "region" : "[113.000, 22.000, 114.000, 23.000]",
>          "domain": 1,
>          "number_domain": 1000,
>          "PM2.5" : [10.0, ..., 10.0],
>          "PM10" : [50.0, ..., 50.0],
>          "NO2" : [50.1, ..., 50.1],
>          "SO2" : [30.0, ..., 30.0],
>          "O3" : [52.1, ..., 52.1],
>          "CO" : [2.1, ..., 2.1],
>          "WS" : [5.0, ..., 5.3],
>          "WD" : ["SE",...,"SE"]
>      }
