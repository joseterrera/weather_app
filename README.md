weather_app
===========

A simple weather app.

This is a simple jquery mobile weather app from Treehouse.


With an api from forecast.io we update the weather on each city this app has. 



What do we need?
3 functions: loadWeather, loadCity, loadDefaultCity.

1. loadWeather has two variables:
latlng: this variable will indicate the city where we are at.

forecastURL: the api key with a "+ latlng" at the end;


loadWeather will have the ajax request with a success method and an error method. 
success: we populate #current_temp and #current_summary with html method (i.e. json.currently.temperature), also for the icon is different, it has 2 parameters( i think the first one indicates what we need to change, and the second one how we intend to change it).

2. loadCity
We need to overwrite the click functionality, so when a user clicks on a city it will call a function loadCity
$("a.city").bind('click', function(){
	loadCity($(this).html);
})

We create the array cities with their latitudes and longitudes.

loadCity: The first thing is to change the location so that it updates to the name that was selected in the left panel. $("#location").html(city)
Next we need to load the weather for that particular city. For that we need to create an associative array(cities) with the coord for each city. (geocoder.us will give you a lat and long for that city).

loadWeather then will access the associative array.

We need to change the loadWeather function to take in the latitude and longitude.

We do that with the variable latlng.
