# Weather Widget

In this exercise you will leverage some APIs in order to fetch and present data in a meaningful way.

There are many useful libraries and frameworks out there, and should you choose to use any then please consider why you chose them and how they contribute to your solution.

Please put emphasis on good application- and code structure, as well as proper object-oriented programming principles and best practices.

Unit testing is important, as well as deciding what to test. Tests are not a requirement for this assignment, but feel free to those that you find make sense.


## About this repo

This repo contains:
- An index.html file
- An assets folder with svg icons
- This readme file

You are encouraged to fork this repo or create a new one if that is more practical.


## Instructions

We would like you to create a website containing two things:
-  A search input field where the user can search for a location
-  A weather widget displaying the weather forecast for the selected location. The widget chould look something like this:

![Weather widget](assets/widget.png)

The widget displays the current weather for a location, and in addition displays the forecast for 3 out of 4 specific times - relative to the current time:
00:00, 06:00, 12:00 and 18:00. 
If the current time is 13:00, it displays the time for 18:00, 00:00 and 06:00,  
if the current time is 05:00, it displays the time for 06:00, 12:00 and 18:00, etc…


### Location data - getting latitude and longitude for a location

The index.html file already contains an input field that will trigger a fetch request on input events.
The fetch request returns an array of location objects which contain information about the location, including the latitude and longitude.

Feel free to use the index.html as a starting point for your solution. If you'd rather start completely fresh, please go ahead!


### Weather forecast data

The data for populating the weather forecast can be retrieved at this endpoint:
https://api.met.no/weatherapi/locationforecast/2.0/complete?lat=63.4468&lon=10.4219

The data returned by the endpoint includes a timeseries array for the weather forecast at the chosen latitude/longitude, where ach object in the contains the forecast for a specific date and time.

Some relevant properties to look for in the objects are:
- object.time
- object.data.instant.details.air_temperature
- object.data.next_1_hours.summary.symbol_code   


### Layout

To keep things simple the widget can have a fixed width and height, but if you want to create a responsive layout and show us some creativity then please go ahead!


### Weather forecast icons

The weather forecast icons you’ll use can be found in the assets folder. 
Their filenames match the values you’ll get in the object.data.next_1_hours.summary.symbol_code


### Bonus

Should you have the time and inclination, here are a few bonus challenges:
- Ensure that the browser remembers the chosen location on reload
- Allow the user to store one or more locations as their favorite, and allow for easy switching between them
- Use Typescript

Please note these are not a requirement of the exercise.


### Good luck
