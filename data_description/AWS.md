## Database: hk_AirQuality_AutomaticWeatherStation_data

- AWS_UST_PIER: automatic weather station, HKUST PIER
- AWS_UST_SEPO: automatic weather station, HKUST SEPO
- AWS_UST_TOWER_B: automatic weather station, HKUST TOWER B
- AWS_YL: automatic weather station, Yuen Long
- AWS_TC: automatic weather station, Tung Chung

***
### AWS_UST_PIER
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW"  
  * temp(Temperature): num (Deg. C) , to the first decimal point 
  * rainfall: num, to the first decimal point 
  * cumulative_rainfall: num, to the first decimal point 
  * SLP(Sea Level Pressure): num(hPa), to the first decimal point
  * irradiance: num, to the first decimal point
  * humidity: num(%), to the first decimal point
  * RSP_Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "temp" : 33.8,
>          "rainfall" : 1.0,
>          "cumulative_rainfall" : 1.0,
>          "SLP" : 1009.0,
>          "irradiance" : 1200.0,
>          "humidity" : 70.0,
>          "RSP_Ozone" : 70.0
>      }

***
### AWS_UST_SEPO
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW" 
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE"
>      }


***
### AWS_UST_TOWER_B
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * temp(Temperature): num (Deg. C) , to the first decimal point 
  * humidity: num(%), to the first decimal point
  * visibility: num(km), to the third decimal point
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "temp" : 1.0,
>          "humidity" : 70.0,
>          "visibility" : 16.000
>      }


***
### AWS_YL
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW" 
  * temp(Temperature): num (Deg. C) , to the first decimal point 
  * rainfall: num, to the first decimal point 
  * cumulative_rainfall: num, to the first decimal point 
  * SLP(Sea Level Pressure): num(hPa), to the first decimal point
  * irradiance: num, to the first decimal point
  * humidity: num(%), to the first decimal point
  * visibility: num(km), to the third decimal point 
  * nitrate_sulfate: num, to the first decimal point  
  * RSP_Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "temp" : 33.8,
>          "rainfall" : 1.0,
>          "cumulative_rainfall" : 1.0,
>          "SLP" : 1009.0,
>          "irradiance" : 1200.0,
>          "humidity" : 70.0,
>          "visibility" : 16.000,
>          "nitrate_sulfate" : 1.0,
>          "RSP_Ozone" : 70.0
>      }

***
### AWS_TC
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * WS(Wind Spd): num (m/s), to the first decimal point 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW"  
  * temp(Temperature): num (Deg. C) , to the first decimal point 
  * rainfall: num, to the first decimal point 
  * cumulative_rainfall: num, to the first decimal point 
  * SLP(Sea Level Pressure): num(hPa), to the first decimal point
  * irradiance: num, to the first decimal point
  * humidity: num(%), to the first decimal point
  * visibility: num(km), to the third decimal point 
  * nitrate_sulfate: num, to the first decimal point  
  * RSP_Ozone: num (ug/m3), to the first decimal point, hourly concentration of Respiratory suspended particulate and Ozone (in separate line)
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "WS" : 1.0,
>          "WD" : "NE",
>          "temp" : 33.8,
>          "rainfall" : 1.0,
>          "cumulative_rainfall" : 1.0,
>          "SLP" : 1009.0,
>          "irradiance" : 1200.0,
>          "humidity" : 70.0,
>          "visibility" : 16.000,
>          "nitrate_sulfate" : 1.0,
>          "RSP_Ozone" : 70.0
>      }

