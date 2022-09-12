# World-Weather-Analysis

## Project Overview

### Overview

Provide a real-time recommendation system to find hotels that fit a client's criteria. Two criteria determine the ideal hotel. First, the hotel must be within a given range of latitude and longitude. Second, acceptable weather conditions for the client's preference.

### Outline

1. **Collect the Data**
   - Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
   - Use the citipy module to list the nearest city to the latitudes and longitudes.
   - Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
   - Parse the JSON data from the API request.
   - Collect the following data from the JSON file and add it to a DataFrame:
     - City, country, and date
     - Latitude and longitude
     - Maximum temperature
     - Humidity
     - Cloudiness
     - Wind speed
2. **Exploratory Analysis with Visualization**
   - Create scatter plots of the weather data for the following comparisons:
     - Latitude versus temperature
     - Latitude versus humidity
     - Latitude versus cloudiness
     - Latitude versus wind speed
   - Determine the correlations for the following weather data:
     - Latitude and temperature
     - Latitude and humidity
     - Latitude and cloudiness
     - Latitude and wind speed
   - Create a series of heatmaps using the Google Maps and Places API that showcases the following:
     - Latitude and temperature
     - Latitude and humidity
     - Latitude and cloudiness
     - Latitude and wind speed
3. **Visualize Travel Data**
   - Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences.
     1. Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
     2. Create a heatmap for the new DataFrame.
     3. Find a hotel from the cities' coordinates using Google's Maps, Places API, and the Search Nearby feature.
     4. Store the name of the first hotel in the DataFrame.
     5. Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.

## Exploratory Analysis with Visualization

### City Latitude vs. Max Temperature

![City Latitude vs. Max Temperature](/weather_data/Fig1.png)

Temperatures become warmer as we approach the equator and being further from the equator results in cooler temperatures.

## Visualize Travel Data

Hotels were located and plotted using the Google Maps API. Locations to search for hotels were selected based on these preferred weather conditions:

- Minimum Temperature: 70 F
- Maximum Temperature: 90 F
- Humidity: Any
- Cloudiness: Any
- Wind Speed: Any

![hotel-spots.png](/Vacation_Search/WeatherPy_vacation_map.png)

## Travel Itinerary Map

Four cities were selected for the customer's travel destination, and a route was then created using the Google Directions API. Finally, the route is displayed on the layer map with pop-up markers of hotels on the route of each city destination.

![WeatherPy_travel_map.png](/Vacation_Itinerary/WeatherPy_travel_map.png)

## Resources

- Data Source: [`cities.csv`](weather_+), [`WeatherPy_vacation.csv`](/Vacation_Search/WeatherPy_vacation.csv), [`WeatherPy_database.csv`](/Weather_Database/WeatherPy_database.csv)
- Libraries: [`pandas`](https://pandas.pydata.org/), [`python-gmaps`](https://python-gmaps.readthedocs.io/en/latest/), [`requests`](https://requests.readthedocs.io/en/latest/), [`matplotlib`](https://matplotlib.org/), [`numpy`](https://numpy.org/), [`citipy`](https://github.com/wingchen/citipy)
- Additional: [OpenWeatherMap API](https://openweathermap.org/api)
- Source Code: [`VacationPy.ipynb`](VacationPy.ipynb), [`WeatherPy.ipynb`](WeatherPy.ipynb)
