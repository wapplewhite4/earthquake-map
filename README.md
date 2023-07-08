# earthquake-map
An interactive earthquake map showing live earthquake data around the globe.
Consists of a series of modules which I completed as part of the Object Oriented Programming in Java course completed though UCSD. Utilized Processing and UnfoldingMaps libraries.

Module 1: 

1:Added code to the setup method and draw method to display two maps side by side in the window.

Module 3: 

1: Modified setup method to create a SimplePointMarker object for each PointFeature in the list features.

2: Added code to the createMarker method to style each marker according to its magnitude.

3: Authored the addKey method, utilizing the PApplet class, to draw a key for the map describing which markers corresponded to which magnitude.

Module 4: 

1: Implemented the isLand(Feature earthquake) method in EarthquakeCityMap.  Method returns true if the location of the input earthquake is on land. Sets "country" property on LandMarker to 	country where earthquake occurred.  Otherwise, location is in ocean and method returns false.

2: Implemented the printQuakes() method in EarthquakeCityMap. Method lists each country in which 1 or more earthquakes occurred and number of earthquakes in that country.

3: Implemented draw() method in CityMarker class. Method draws a triangle marker for each city.

4: Implemented drawEarthquake() method in LandQuakeMarker and OceanQuakeMarker. Method draws LandQuakeMarkers as circles and OceanQuakeMarkers as squares. Scales size of marker based on magnitude.

5: Implemented colorDetermine() method in EarthquakeMarker. Method colors markers depending on whether they are shallow, intermediate, or deep.

Module 5: 

1: Changed class hierarchy structure so that CityMarker extends CommonMarker instead of SimplePointMarker.

2: Implemented the selectMarkerIfHover helper method in EarthquakeCityMap. Method sets the instance variable selected for the first Marker it finds that mouseX and mouseY is inside of.

3: Implemented the showTitle(PGraphics pg, float x, float y) in both EarthquakeMarker and CityMarker. Method displays relevant information about earthquakes and cities when mouse is hovered.

4: Implemented the mouseClicked() method in EarthquakeCityMap. Method tests whether the lastClick variable refers to a null object or not; if lastClick is not null, this click “de-selects” 	whichever marker was clicked on last and so all markers should be displayed.  Otherwise, the method must determine which marker is being selected (if any) and hide / display other markers so that: When an earthquake’s marker is selected, all cities within the threat circle of this earthquake are displayed on the map and all other cities and earthquakes are hidden. When a city’s marker is selected, all earthquakes which contain that city in their threat circle are displayed on the map and all other cities and earthquakes are hidden.

Module 6: 

1: Implemented the Comparable interface in EarthquakeMarker. Implemented the compareTo(EarthquakeMarker marker) method in the EarthquakeMarker class so that it sorted earthquakes in reverse order of magnitude.

2: Implemented the private method void sortAndPrint(int numToPrint) in EarthquakeCityMap. Method will create a new array from the list of earthquake markers. Then it will sort the array of earthquake markers in reverse order of their magnitude (highest to lowest) and then print out the top numToPrint earthquakes.

3: Added extension to project to color countries based on life expectancy data form the World Bank. 

4: Authored loadTop20QuakesFromCSV(PApplet p, String fileName) method to parse in the top 20 earthquakes by magnitude from 1900-2000.

5: Added functionality to display white circle behind earthquake markers which was sized based on the threat radius of the quake.

Final Course Grade: 94.85%
