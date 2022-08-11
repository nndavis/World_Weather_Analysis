# World_Weather_Analysis
 
## Introduction
In this project I was to retrieve weather data, create a customer travel destinations map, and create a travel itinerary map. In theory, this would be used for a "PlanMyTrip" app, so taking user input for location and weather preference is important. 

## Analysis
This project consists of many dataframes and API calls from google maps and OpenWeatherMap. To start I created 2,000 random lat and lon to create coordinates, and using those coordinates i located the nearest city using citipy. OpenWeatherMap was used to find lat, long, max temp, humidity, cloudiness, wind speed, and weather descriptions for each of those cities. That info was put into a new dataframe and exported as a csv. This was done under the Weather_Data folder.
The next step was to take user input to find which cities they would like to travel to. Once temperature preferences were added I made an API call using their input and my dataframes to generate a map using gmaps and marked the cities that fell into the temperature range. This was done under the Vacation_Search folder.
Lastly, a travel itinerary map was created using google directions API. This pulled routes from the chosen city cities. to_numpy was a key function here, as it retrieved latitude-longitude pairs as tuples from each city dataframe. As well as concat(), because once I had each dataframe for each city made they needed to be combined so i was able to use gmaps to show hotel name, city, country, and weather data on the map with markers. This was done under the Vacation_Itinerary folder.
