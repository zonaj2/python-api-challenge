# python-api-challenge

## Table of Contents
* [Tools](#tools)
* [WeatherPy](#weatherpy)
* [VacationPy](#vacationpy)
* [Analysis](#analysis)

## Tools
- Python library: citipy, geoViews
- API: OpenWeatherMap, Geoapify
- JSON
- Jupyter

### WeatherPy: 
Used Python requests, APIs, and JSON traversals to answer  
`What is weather like as we approach the equator?`

#### Key Steps:
Generated random geographic coordinates and a list of cities using `citypy`. 

Used the OpenWeatherMap API to retrieve weather data from the generated cities list. Exported the city data to a .csv file (city_data.csv)

Created a series of scatter plots to showcase the following:
* Latitude vs. Temperature 
* Latitude vs. Humidity 
* Latitude vs. Cloudiness 
* Latitude vs. Wind Speed

Computed the linear regression for each relationship above. The plots were separated into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). A function was defined in order to create linear regression plots across all the relationships.This function was used to create a series of scatter plots for each relationship. A linear regression line, the model's formula, and the r values were included in the visualization.

### VacationPy: 
Used Python requests, APIs, and JSON traversals to answer:  
`How can we use weather data to plan future vacations according to our ideal weather conditions?`  
I defined my ideal weather conditions as cities with Humidity >= 40% and Temperature <= 70 degrees F.  

Created map visualizations using Geoapify API and geoViews Python library.
The list of cities and weather data generated in Part 1 was used to plan future vacations. The main focus was to use the Geoapify API and the geoViews Python library to employ Python skills to create map visualizations.

#### Key Steps:
A map was created that displayed a point for every city in the city_data_df DataFrame. The size of the point was the humidity in each city.  

The DataFrame was narrowed down to my ideal weather conditions, which was less than 50% humidity and a maximum temperature less than 28 degress celsius.  

The filtered data was used to create a new Dataframe called hotel_df, which brought in the city, country, coordinates and humidity.  

For each city, Geoapify API was used to find the first hotel located within 10,000 meters of the city's coordinates and plot on to a new map.  

The hotel name and the country were added as additional information in the hover message for each city on the map.  


### Analysis
