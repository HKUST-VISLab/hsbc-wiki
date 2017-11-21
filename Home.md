# Database Description
<img src="https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/imgs/praise_201703_tagline-1024x230.png?raw=true" width="300px">

# Resource

The project consists following five database:

* [Weather and AQ from offical websites](https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/database_description/weather_aq_public.md)
* [Weather and AQ from ENVF](https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/database_description/weather_aq_hkust.md)
* [Traffic](https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/database_description/Traffic.md)
* [POI](https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/database_description/POI.md)
* [Map](https://github.com/HKUST-VISLab/hsbc-wiki/blob/master/database_description/Map.md)

Created by HKUST VISLab, this repo describe the databased design forUrban Informatics and Big Data Analytics (PARISE-HK, Task 3). 
The databases are designed to store heterogeneous data affecting or describing the air quality in cities. 
 
## Ref link of this project
* [Back end](https://github.com/HKUST-VISLab/hsbc-back-end): Data processing, initial database, models
* [Web server](https://github.com/HKUST-VISLab/hsbc-web-server-analytics)
* [Front end system](https://github.com/HKUST-VISLab/hsbc-front-end-analytics)


## Installing 
Please run the command bellow after cloning this repository.

> git config --local include.path ../.gitremote

If you just want to modify the wiki without publishing them to other repository **hsbc-back-end** and **hsbc-front-end** and **hsbc-webserver**, please use the command 
> git push.

You can also specify the repo you want to modify by the command
> git push back-end(or front-end, or web-server)

If you want to publish the wiki to all repositories, please use the command 
> git push all.