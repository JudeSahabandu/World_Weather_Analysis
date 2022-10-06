# World_Weather_Analysis

---

## Purpose of Analysis

This analysis uses APIs to build a interactive solution for travellers. The map allows our users to determine thier travel destinations based on thier preferred weather data inputs. Furthermore, the usage of APIs enables the user to develop a travel itinerary which includes the following details;

1. Cities to vist based on weather preferences
2. Description of the weather data
3. Nearest hotel to the selected city coordinates
4. Travel directions between selected cities

The below points summarize the approach in brief to develop the above application.

### Retrieving World Weather Data

The following points were crucial in retreiving world weather data;

* Generating a random list of 2000 latitudes and longitudes using random.uniform() function
* Filtering through random coordinates and assigning cities to usable coordinates with the citipy module
* Importing the open weather maps api and building the end point ulr
* Retreiving weather data through an API call and try-except block
* Storing Data in a DataFrame and exporting into a csv file for further analysis

### Customer Travel Destination Map

Upon storing the weather data across global cities in a csv file, the following steps were used to determine vacation spots for travellers based on thier weather preferences;

* Using input statements to obtain weather preferences
* Using the loc method to create a new DataFrame with cities within regions of preferred weather parameters
* Using Google Maps API to identify closest hotels to selected coordinates within regions of preferred weather parameters
* Storing Data in a DataFrame and exporting into a csv file for further analysis
* Develop a map with markers on regions of preferred weather parameters

### Travel Itinerary Map

In the final step of our interative travel solution, we develop a travel itinerary out of the preferred travel destinations;

* Setting up travel markers by creating a marker layout map with preferred travel destination results
* Select 4 travel destinations and setting their own DataFrames using the loc method
* Using the to_numpy() function and list indexing to retreive latitude and longitude data for each city in the DataFrame
* Using the Google Maps Directions API to set the travel plan across the selected cities
* Develop a map with markers on the selected travel itinerary and the directions between selected cities

