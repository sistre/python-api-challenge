# python-api-challenge
Python API Homework - What's the Weather Like?
Sean Istre

# The Assignment
The Python API Challenge consists of two parts WeatherPy and VacationPy. Together, the two parts pull, analyze, graph, map data pertaining to city weather data.

## Part I - WeatherPy
WeatherPy creates a visualizes the weather of 500+ randomly selected cities across the world of varying distance from the equator. The data is pulled using the OpenWeatherMap API. It removes the duplicate locations and locations for which the OpenWeatherMap API has no data.

From the weather data for each city it creates a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

Next it runs linear regression on each relationship, this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

It also stores the city and weather data to a CSV file to use in part II.

## Part II - VacationPy
VacationPy uses the Google Places API and the data from part I to help find potential great vacation spots.

1. It creates a heat map that displays the humidity for every city from the part I of the homework.
2. From the part I data it filters the cities down to those with favorable weather conditions.
3. Next it uses the Google Places API to find the first hotel for each city located within 5000 meters of it's coordinates.
4. Last it plots the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

