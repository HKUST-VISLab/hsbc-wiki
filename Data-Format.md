## Database collections
* station
* air_station
* weather_code
* air_quality
* current_weather
* forecast_weather
* last_update 
***
### station
54 weather stations
16 among them has forecast_weather info
others only have current_weather info
  * _id: an object id created by mongodb
  * longitude: string, to the sixth decimal point
  * latitude: string, to the sixth decimal point
  * webcam_angle: string, a multiple of 45, between [0, 360]
  * has_forecast: bool
  * wind_longitude: string, "" or a number to the sixth decimal point
  * wind_latitude: string, "" or a number to the sixth decimal point
  * station_code: string, three uppercase letter
  * station_name: string, simplified Chinese

an example
>      {
>          "_id" : ObjectId("59145f9ae177d259648c7fc6"), 
>          "longitude" : "114.174297",
>          "webcam_angle" : "0",
>          "has_forecast" : true,
>          "wind_longitude" : "",
>          "station_code" : "hko",
>          "latitude" : "22.301944",
>          "wind_latitude" : "",
>          "station_name" : "香港天文台"
>      }
***
### air_station
16 air quality stations
  * _id: an object id created by mongodb
  * station_name: string, a capitalized English name

an example
>      {
>          "_id" : ObjectId("59145f9ae177d259648c7ffc"),
>          "station_name" : "Central/Western"
>      }
***
### weather_code
  * _id: an object id created by mongodb
  * code: string, 2 digitals
  * schi: string, simplified Chinese
  * tchi: string, traditional Chinese
  * eng: string, capitalized English

an example
>      {
>          "_id" : ObjectId("59145f9ae177d259648c800c"),
>          "schi" : "雨",
>          "tchi" : "雨",
>          "code" : "63",
>          "eng" : "Rain"
>      }
***
### air_quality
  * _id: an object id created by mongodb
  * update_time: string, time in the format of "%Y-%m-%d %H:%M:%S"
  * CO: null or a string,
  * station_name: string, a capitalized English name
  * AQHI: num, to the first decimal point
  * PM10: num, to the first decimal point
  * SO2: num, to the first decimal point
  * NO2: num, to the first decimal point
  * O3: num, to the first decimal point
  * PM2_5: num, to the first decimal point
an example
>      {
>          "_id" : ObjectId("59145f9bda8f5d922aa337da"),
>          "update_time" : "2017-05-11 20:00:00",
>          "CO" : null,
>          "station_name" : "Central/Western",
>          "AQHI" : 3.0,
>          "PM10" : 22.8,
>          "SO2" : 14.0,
>          "NO2" : 73.4,
>          "O3" : 16.6,
>          "PM2_5" : 15.3
>      }
***
### current_weather

an example
>      {
>          "_id" : ObjectId("59145f9cda8f5d922aa337ea"),
>          "visibility" : "",
>          "winddirection" : "",
>          "time" : "2017-05-11 20:50:00",
>          "temp" : "26.7",
>          "mintemp" : "25.7",
>          "stn" : "HKO",
>          "windspeed" : "",
>          "pressure" : "1013.1",
>          "gust" : "",
>          "grasstemp" : "",
>          "maxtemp" : "31.6",
>          "rh" : "87",
>          "grassmintemp" : ""
>      }
***
### forecast_weather

  * _id: an object id created by mongdb,
  * longitude: num, to the third decimal point,
  * daily_forecast: an array of 10 objects,
  * hourly_weather_forecast: an array of 231 objects,
  * model_time: string, time in the format "%Y-%m-%d %H:%M:%S", 
  * station_code: string, three uppercase letter, ,
  * latitude: num, to the third decimal point
  * last_modified: string, time in the format "%Y-%m-%d %H:%M:%S", 

an example
>      {
>          "_id" : ObjectId("59145f9dda8f5d922aa33820"),
>          "longitude" : 114.174,
>          "daily_forecast" : [object_0, object_1, ... ,object_9 ],
>          "hourly_weather_forecast" : [object_0, object_1, ... ,object_230 ],
>          "model_time" : "2017-05-10 12:00:00",
>          "station_code" : "TKL",
>          "latitude" : 22.529,
>          "last_modified" : "2017-05-11 20:55:28"
>      }

the objects in the array of "hourly_weather_forecast", every hour for the next 231 hour
>        {
>            "forecast_temperature" : 23.7,
>            "forecast_relative_humidity" : 87.8,
>            "forecast_hour" : "2017-05-21 00:00:00",
>            "forecast_wind_speed" : 5.1,
>            "forecast_wind_direction" : 86.0
>        }

the objects in the array of "daily_forecast", everyday for the next 10 days
>        {
>            "forecast_daily_weather" : 52,
>            "forecast_date" : "2017-05-11 00:00:00",
>            "forecast_maximum_temperature" : 26.7,
>            "forecast_chance_of_rain" : "< 10%",
>            "forecast_minimum_temperature" : 25.8
>        },
***
### last_update
record the last modified time of every collections
an example
>        {
>            "_id" : ObjectId("59145f9ada8f5d922aa337d3"),
>            "last_update_time" : "2017-05-11 21:40:00",
>            "collection_name" : "current_weather"
>        }
