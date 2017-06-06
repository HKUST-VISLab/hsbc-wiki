## Database: Regional_GTS_data

- Regional_GTS_SYNOP: This is mainly based on surface weather information (SYNOP) available on the GTS network. There are eight plots on this page, including Precipitation, Temperature, Dew Point, Sea Level Pressure, Wind Speed, Wind Direction, Relative Humidity and Visibility. These plots are updated once every three hours.
- Regional_GTS_METAR: This is mainly based on hourly aviation weather reports (METAR) available on the GTS network. There are six plots on this page, including Temperature, Dew Point, Wind Speed, Wind Direction, Sea Level Pressure and Visibility. These plots are updated once every hour. 

***
### Regional_GTS_SYNOP
  * _id: an object id created by mongodb
  * area: [Lat1,Lng1,Lat2,Lng2], regional area 
  * region: String, "N/A", "Hong Kong", "Peral River Delta", "Guang Dong", "Southern China", "China", "Southeast Asia"
  * time: string, UTC time in the format of "%Y-%m-%d %H:%M"
  * precipitation: num(mm), to the first decimal point
  * temp(Air Temperature): num (Deg. C) , to the first decimal point 
  * dew(Dew Point): num (Deg. C) , to the first decimal point
  * SLP(Sea Level Pressure): num(hPa), to the first decimal point
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): String(Degree), "N","NE","E","SE","S","SW","W","NW"
  * humidity: num(%), to the first decimal point 
  * visibility: num(km), to the third decimal point 
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "time" : "2012-06-06 00:00",
>          "area" : [113.8,22.1,114.5,22.7],
>          "region" : "Hong Kong",
>          "precipitation" : 1.0,
>          "temp" : 33.8,
>          "dew" : 16.0,
>          "SLP" : 1009.0,
>          "WS" : 1.0,
>          "WD" : "NE",
>          "humidity" : 70.0,
>          "visibility" : 16.000 
>      }


***
### Regional_GTS_METAR
  * _id: an object id created by mongodb
  * area: [Lat1,Lng1,Lat2,Lng2], regional area 
  * region: String, "N/A", "Hong Kong", "Peral River Delta", "Guang Dong", "Southern China", "China", "Southeast Asia"
  * time: string, UTC time in the format of "%Y-%m-%d %H:%M"
  * temp(Air Temperature): num (Deg. C) , to the first decimal point 
  * dew(Dew Point): num (Deg. C) , to the first decimal point
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): String(Degree), "N","NE","E","SE","S","SW","W","NW"
  * humidity: num(%), to the first decimal point 
  * visibility: num(km), to the third decimal point 
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "time" : "2012-06-06 00:00",
>          "area" : [113.8,22.1,114.5,22.7],
>          "region" : "Hong Kong",
>          "temp" : 33.8,
>          "dew" : 16.0,
>          "WS" : 1.0,
>          "WD" : "NE",
>          "humidity" : 70.0,
>          "visibility" : 16.000 
>      }
