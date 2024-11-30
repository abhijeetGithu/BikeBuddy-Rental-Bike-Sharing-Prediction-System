# BikeBuddy-Rental-Bike-Sharing-Prediction-System

**Project Description**

BikeBuddy is a modern bike-sharing system solution to automate processes from sign up to rental and return. Bike-sharing, with more than 500 programs worldwide and over 500,000 bicycles in operation, provides a meaningful contribution to traffic management, environmental management, and health care issues.

This work aims at developing an end-to-end regression system to estimate bike rental counts from user provided information. Using hyper-trained machine learning models, it guarantees very accurate predictions. Flexible deployment is also provided by the system and enables users to adapt systems to their requirements.

_________________

## About Dataset


The bike-sharing rental process is significantly influenced by environmental and seasonal factors such as weather conditions, precipitation, day of the week, season, and time of day. This project utilizes a two-year historical dataset (2011–2012) from the Capital Bikeshare system in Washington D.C., USA, available at http://capitalbikeshare.com/system-data. We aggregated the data on two hourly and daily basis and then 
extracted and added the corresponding weather and seasonal information. Weather information are extracted from http://www.freemeteo.com. 


**Associated tasks**


	- Regression: 
		Predication of bike rental count hourly or daily based on the environmental and seasonal settings.
	
	- Event and Anomaly Detection:  
		Count of rented bikes are also correlated to some events in the town which easily are traceable via search engines.
		For instance, query like "2012-10-30 washington d.c." in Google returns related results to Hurricane Sandy. Some of the important events are 
		identified in [1]. Therefore the data can be used for validation of anomaly or event detection algorithms as well.


**Files**

	- Readme.txt
	- hour.csv : bike sharing counts aggregated on hourly basis. Records: 17379 hours
	- day.csv - bike sharing counts aggregated on daily basis. Records: 731 days

**Dataset characteristics**

Both hour.csv and day.csv have the following fields, except hr which is not available in day.csv
	
	- instant: record index
	- dteday : date
	- season : season (1:springer, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2011, 1:2012)
	- mnth : month ( 1 to 12)
	- hr : hour (0 to 23)
	- holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : Normalized temperature in Celsius. The values are divided to 41 (max)
	- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
	- hum: Normalized humidity. The values are divided to 100 (max)
	- windspeed: Normalized wind speed. The values are divided to 67 (max)
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered


## Project screenshot

**Daily Based Dataset Count**
<center> <img src="static/day.jpg"> </center>


**Hourly Based Dataset Count** 
<center> <img src="static/hr.jpg"> </center>

