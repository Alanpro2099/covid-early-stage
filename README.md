# Covid cases and ratios world wide in early 2021
## Visit and interact with this webpage dashboard by clicking my GitHub page link:
https://alanpro2099.github.io/covid-early-stage/

This webpage is focusing on the covid cases worldwide. Two datasets have been explored. The first one is a world population dataset with polygon geometry information which is used as a tileset for Mapbox application. Then a monochrome light style is created, and a layer is added to it by using this resource. The second dataset is a current total covid cases for individual country. Because it only has a point geometry information, it is mainly used for data analysis combined with the first dataset together to generate a double axes bar chart.

The dataset is very large. It would make more senses to focus on the top 15 countries in terms of total covid cases. The data is sorted descendingly by total covid cases and then the top 15 features are taken to plot the bar chat. The total covid cases alone is not very informative as different countries differentiates largely in size and population. Calculating the ratio of covid cases to the population is a legit indicator of the severity of the epidemic situation. A nested for loop is used to match the two datasets item to calculate the ratio. The total cases are used as the left y axis and the ratio is used as the right y axis; the bars for the ratios are made wider to suggest importance. This is plotted by chart.js. All the data processing is done by JavaScript. The bar plot is tailored in a careful way to make it visually pleasant. Then a doughnut plot presenting the total covid cases in the top 15 countries serves as a complement.

A world population map is added to the bottom of webpage. Two colour themes are implemented to represent the population categories in the world map, because countries’ population sizes can vary greatly. Originally, the Mapbox light style is used to increase the ink ratio, however it is too simple. Some countries with similar population and adjacent to each other has similar colour and it is very difficult to distinguish. ‘Country-boundaries-v1’ tileset is deployed to add the boundary layer. By making the area fill colour transparent, it only adds the boundary line. Then a water layer from ‘mapbox-streets-v8’ tileset is also added to make some countries distinguishable from the ocean and the overall map more vivid looking. Opacity is adjusted in the way when zooming in, the colour of each country becomes more intensive along with the emerging of country labels. A legend is added to show the population category information. Navigation bar, scale bar, full screen button and the geocoder search bar are also added. In the code, ‘map.queryRenderedFeatures’ function allows the user to retrieve country information when mouse hovering over it on the map. Country information is shown at the Infor panel at the top-left corner. When a mouse is over a country, its point shape is changed into a hand. When you click a country, a popup will appear to show more features information of the country.

There are many other interactivities added. The bar chart is the core. When hovering over a bar, its border becomes solid. Then when you click a bar, the colour of the bar will change to grey. The elements’ information is retrieved from console. Bar index information is used to trigger a flash of the corresponding piece in the doughnut chart by changing the meta data background colour of chart2. It is also used to find the country’s name and then fed to ‘Wikipedia rest_v1’ api to get a country’s summary, which will be shown at the bottom of the bar chart. Moreover, ‘map.setFilter’ function is utilised to filter all the other countries except this country in the world population map. When a click a bar, there are changes in all elements of the webpage. Then you will click an empty space in the bar chart to reset the world map. Because now the ‘elements’ is an empty array; this will do nothing but reset the map. When you click one bar you can see the changes happen in all the elements of the webpage. 

### Appendix

Thomas, A, Lab 4, 5, 6, 7, GEOM90007 information visualisation, School of Computing and Information Systems, Melbourne University, Melbourne, Vic., September 2021.
Chart plotting and JavaScript part refers to Chart.js documentation:
Chartjs.org, 2021. [Online]. Available: https://www.chartjs.org/docs/latest/.
The Mapbox documentation are also used as reference:
"Documentation", Mapbox, 2021. [Online]. Available: https://docs.mapbox.com/. [Accessed: 19- Sep- 2021].
The world population data comes from:
"MinnPost", GitHub, 2021. [Online]. Available: https://github.com/MinnPost. [Accessed: 19- Sep- 2021].
 
Chart.js | Chart.js",
 [Accessed: 19- Sep- 2021].
 “The current total covid cases in each country data comes from:
  Cases country",
Coronavirus-resources.esri.com
, 2021. [Online]. Available: https://coronavirus-
 resources.esri.com/datasets/bbb2e4f589ba40d692fab712ae37b9ac_2/explore?location=2.758326%2C
 