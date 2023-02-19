# python-api-challenge

## WeatherPy

### Part 1:
The goal of the WeatherPy was to visualize the weather of over 500 cities of varying distances from the equator by analyzing the relationship between weather variables and latitude.

To accomlish this task, I used the OpenWeatherMap API to retrieve weather data from the cities list that was pre-generated. After creating a cities list, I performed the API calls to OpenWeatherMap. After retrieving the results, I converted the raw data to a dataframe. I then inspected the data to remove the cities where Humidty was greater than 100%. Once the data reflected cities with humidity <100%, I created plots to showcase the relationship between weather variables and latitude. 

The scatter plots to showcased the following relationships:

#### Latitude vs. Temperature

Findings: As latitude increases away from the equator, the max temperature decreases.

#### Latitude vs. Humidity

Findings: There is no direct relationship between latitude and humidity, as data across several points of latitude have 100% humidity.

#### Latitude vs. Cloudiness

Findings: There is no direct relationship between latitude and cloudiness, as data across several points of latitude have anywhere from 0-100% cloudiness.

#### Latitude vs. Wind Speed
Findings: Wind speed remains relatively consistent, predominantly in the range of 0-10 mph, across all latitudes.

### Part 2:
Afterwards, I computed the linear regression for each relationship. First, I seperated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). The plots showcased the following relationships:

#### Northern Hemisphere: Temperature vs. Latitude
In the northern hemisphere, Max Temp vs. Latitude has a strong negative correlation.

#### Southern Hemisphere: Temperature vs. Latitude
In the southern hemisphere, Max Temp vs. Latitude has a moderate positive correlation.

#### Northern Hemisphere: Humidity vs. Latitude
In the northern hemisphere, Humidity (%) vs. Latitude has no correlation.

#### Southern Hemisphere: Humidity vs. Latitude
In the southern hemisphere, Humidity (%) vs. Latitude has a weak correlation.

#### Northern Hemisphere: Cloudiness vs. Latitude
In the northern hemisphere, Cloudiness (%) vs. Latitude has no correlation.

#### Southern Hemisphere: Cloudiness vs. Latitude
In the southern hemisphere, Cloudiness (%) vs. Latitude has no correlation.

#### Northern Hemisphere: Wind Speed vs. Latitude
In the northern hemisphere, Wind Speed (mph) vs. Latitude has no correlation.

#### Southern Hemisphere: Wind Speed vs. Latitude
In the southern hemisphere, Wind Speed (mph) vs. Latitude has a weak correlation.

## VacationPy

The goal of this section was to use the Geoapify API and the geoViews Python library to plan future vacation location using map visualizations.
First, I configured gmaps to create a map, using Lat and Lng as locations and humidity as the weight. I also added a heatmap layer to the map.

I then created a new dataframe, narrowing down the data to fit ideal weatehr criteria, such as a max temperture between 60 degrees and 75 degrees, zero cloudiness and wind speed less than 10 m/s. As a result, the dataset was narrowed down to 19 cities in total. 

I then stored the data into a new variable named hotel_df and prepared to run API calls from Google Places to retrieve hotel data for each of the cities. Once the API call was run and the nearest hotel data was populated in hotel_df, I configured the marker layer as well as added hotel marks to the heatmap. 

As a result, I was able to create two maps highlighting weather conditions for locations across the globe, one of which matches interest for ideal vacation destinations.



