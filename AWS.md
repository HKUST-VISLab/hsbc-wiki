## Database: hk_AirQuality_AutomaticWeatherStation_data

- AWS_UST_PIER
- AWS_UST_SEPO
- AWS_YL
- AWS_TC


### AWS_UST_PIER(automatic weather station, HKUST PIER)
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW", Wind Direction 
  * Temp(Temperature): num (Deg. C) , to the first decimal point, Temperature 
  * Rainfall: num, to the first decimal point 
  * Cumulative Rainfall: num, to the first decimal point 
  * Sea Level Pressure: num, to the first decimal point
  * Irradiance: num, to the first decimal point
  * Relative Humidity: num, to the first decimal point
  * RSP & Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "Temp" : 33.8,
>          "Rainfall" : 1.0,
>          "Cumulative Rainfall" : 1.0,
>          "Sea Level Pressure" : 1009.0,
>          "Irradiance" : 1200.0,
>          "Relative Humidity" : 70.0,
>          "RSP & Ozone" : 70.0
>      }
***

### AWS_UST_SEPO(automatic weather station, HKUST SEPO)
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW", Wind Direction 
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE"
>      }
***

### AWS_YL(automatic weather station, Yuen Long)
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW", Wind Direction 
  * Temp(Temperature): num (Deg. C) , to the first decimal point, Temperature 
  * Rainfall: num, to the first decimal point 
  * Cumulative Rainfall: num, to the first decimal point 
  * Sea Level Pressure: num, to the first decimal point
  * Irradiance: num, to the first decimal point
  * Relative Humidity: num, to the first decimal point
  * Visibility: num, to the third decimal point 
  * Nitrate & Sulfate: num, to the first decimal point  
  * RSP & Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "Temp" : 33.8,
>          "Rainfall" : 1.0,
>          "Cumulative Rainfall" : 1.0,
>          "Sea Level Pressure" : 1009.0,
>          "Irradiance" : 1200.0,
>          "Relative Humidity" : 70.0,
>          "Visibility" : 16.000,
>          "Nitrate & Sulfate" : 1.0,
>          "RSP & Ozone" : 70.0
>      }
***
### AWS_TC(automatic weather station, Tung Chung)
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW", Wind Direction 
  * Temp(Temperature): num (Deg. C) , to the first decimal point, Temperature 
  * Rainfall: num, to the first decimal point 
  * Cumulative Rainfall: num, to the first decimal point 
  * Sea Level Pressure: num, to the first decimal point
  * Irradiance: num, to the first decimal point
  * Relative Humidity: num, to the first decimal point
  * Visibility: num, to the third decimal point 
  * Nitrate & Sulfate: num, to the first decimal point  
  * RSP & Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "Temp" : 33.8,
>          "Rainfall" : 1.0,
>          "Cumulative Rainfall" : 1.0,
>          "Sea Level Pressure" : 1009.0,
>          "Irradiance" : 1200.0,
>          "Relative Humidity" : 70.0,
>          "Visibility" : 16.000,
>          "Nitrate & Sulfate" : 1.0,
>          "RSP & Ozone" : 70.0
>      }

