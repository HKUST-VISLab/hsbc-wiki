## Database: hk_AirQuality_data

- air_quality
- AWS 

***
### air_quality
  * _id: an object id created by mongodb
  * update_date: string, time in the format of "%Y-%m-%d %H:%M:%S"
  * station_name: string, "CL"(Central), "CB"(Causeway Bay), "MK"(Mong Kok),  "TC"(Tung Chung), "YL"(Yuen Long), "TW"(Tsuen Wan), "KC"(Kwai Chung), "CW"(Central Western), "SP"(Sham Shui Po), "TP"(Tai Po), "ST"(Sha Tin), "KT"(Kwun Tong), "EN"(Eastern), "TM"(Tap Mun)
  * AQHI: num, to the first decimal point, air quality health index
  * AQI: num, to the first decimal point, air quality index
  * RSP: num (ug/m3), to the first decimal point, Respiratory suspended particulate hourly concentration   
  * FSP: num (ug/m3), to the first decimal point, Fine Suspended Particulates  hourly concentration
  * NO2: num (ppb), to the first decimal point,  hourly concentration  
  * SO2: num (ppb), to the first decimal point,  hourly concentration
  * O3: num (ppb), to the first decimal point,  hourly concentration
  * CO: num (ppm), to the first decimal point,  hourly concentration
  * temp(Temperature): num (Deg. C) , to the first decimal point, Temperature 
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N", "E", "S", "W", Wind Direction 
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_date" : "2017-06-06",
>          "station_name" : "CW",
>          "AQHI" : 2.0,
>          "AQI" : 23.0,
>          "RSP" : ,
>          "FSP" : ,
>          "NO2" : 73.4,
>          "SO2" : 14.0,
>          "O3" : 16.6,
>          "CO" : ,
>          "temp" : 22.8,
>          "WS" : ,
>          "WD" : 
>      }

***
### AWS
  * _id: an object id created by mongodb
  * update_date: string, date in the format of "%Y-%m-%d"  
  * station_name: string, "TC"(Tung Chung), "YL"(Yuen Long),  "HKUST_Pier"(HKUST Pier), "HKUST_SEPO"(HKUST SEPO) 
  * WS(Wind Spd): num (m/s), to the first decimal point, Wind Speed 
  * WD(Wind Dir): char (Degree), "N","NE","E","SE","S","SW","W","NW", Wind Direction 
  * temp(Temperature): num (Deg. C) , to the first decimal point, Temperature 
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
>          "station_name" : "TC",
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


