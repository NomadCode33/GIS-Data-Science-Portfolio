# Population Interactive Map
The project involved retrieving King County census data and constructing an interactive HTML map. It features three datasets: population data for 2000 and 2010, and poverty data for 2012-2016. Users can switch between these datasets using buttons, enhancing the viewing experience through reliable, user-friendly visualizations.

**Link to project:** https://t3ch12et.github.io/Population%20Interactive%20Map/

<img src="./Population Interactive Map.gif" img alt = "Population GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON

The project embarked on an intriguing journey with the retrieval of King County census data, focusing on the population statistics. This initial step allowed me to delve into the dataset, laying the groundwork for constructing an interactive HTML document. The objective was clear: to create a dynamic map showcasing three distinct datasets for King County. These datasets included the census tract population for the years 2000 and 2010, and a poverty map for the same region.

To achieve this, I incorporated a button feature that effortlessly switches between the different datasets, enhancing the viewer's experience by providing a seamless transition between the maps. The use of reliable and esteemed datasets was paramount, ensuring the accuracy and credibility of the visualizations. My goal was to create an engaging, user-friendly interface that allowed users to interact with the data intuitively, thus gaining a deeper understanding of the demographic changes over the years.

Here's a detailed look into the process:

1. **HTML Structure and Dependencies:**
   - The document commenced with the `<!DOCTYPE html>` declaration, followed by the basic HTML structure comprising `<html>`, `<head>`, and `<body>` tags.
   - Within the `<head>` section, a title was defined, along with a link to the Leaflet CSS file to style the map.
   - The `<body>` section included scripts for Leaflet, a JavaScript library for maps, jQuery for handling AJAX requests, and an external GeoJSON file named `KCPop2000.js`.

2. **Leaflet and Map Initialization:**
   - A `<div>` element with the ID `mapid` was created to house the map, with specified dimensions (800px by 600px) and centered using CSS.
   - A Leaflet map, referred to as `mymap`, was initialized with the center point set to Seattle’s coordinates (latitude: 47.6062, longitude: -122.3321) and a zoom level of 10.
   - A tile layer from OpenStreetMap was added to provide the base map tiles.

3. **Styling and Classification Functions:**
   - Functions such as `popStyle`, `classification`, `newStyle`, and `oldStyle` were defined to style the population data for the year 2000.
   - The classification function categorized the population data into various ranges, assigning corresponding colors for better visual distinction.
   - The `newStyle` and `oldStyle` functions handled mouse hover effects to highlight the tract boundaries, enhancing interactivity.

4. **Popup Functions for Population Data:**
   - Functions like `popUp2000` and `popUp2010` were implemented to bind popups to map layers, displaying census tract names and population data for the years 2000 and 2010 respectively.
   - These functions also managed mouse events to show or hide popups and change styles on hover, providing an interactive user experience.

5. **Styling and Popup Functions for Poverty Data:**
   - Functions such as `povStyle` and `povclass` were designed for styling poverty data based on different percentage ranges.
   - The `povUp200` function was responsible for binding popups to display poverty data for each census tract, with similar mouse event handling as the population functions.

6. **GeoJSON Data Layers:**
   - Three GeoJSON layers were defined: `pop2000Layer` for the year 2000 population data, `pop2010Layer` for 2010 population data, and `povper200Layer` for poverty percentage data.
   - Data for `pop2010Layer` and `povper200Layer` were loaded asynchronously using jQuery’s `$.getJSON` method from specified URLs.

7. **Layer Control Functions:**
   - Functions such as `pop2000`, `pop2010`, and `povper200` were implemented to add the corresponding data layer to the map and remove the others.
   - These functions ensured that only one layer was visible at a time, maintaining a clean and focused visualization.

8. **Control Buttons:**
   - Three buttons were created to switch between the different data layers. Each button called one of the layer control functions (`pop2000`, `pop2010`, `povper200`) upon being clicked, allowing users to seamlessly toggle between the datasets.

This meticulously crafted code leveraged Leaflet and GeoJSON to create an interactive map that vividly visualized demographic data. The ability to switch between various datasets with ease provided users with a comprehensive tool to explore and understand the demographic shifts and economic conditions within King County over time.

## Optimizations

Exploring the website, several optimizations stand out that significantly enhanced the project's functionality and user experience. The seamless integration of Leaflet and GeoJSON provided a robust framework for interactive mapping, ensuring smooth and responsive map interactions. The implementation of intuitive buttons to switch between different datasets allowed users to easily navigate through various data layers, providing a clear and comprehensive view of King County's demographic changes. The thoughtful use of color classification and hover effects brought the data to life, making it visually appealing and easier to interpret. These optimizations collectively created an engaging and informative tool that effectively communicated complex demographic information.

While the project already excels in many areas, there are still opportunities for further enhancement. Improving the loading speed of the map layers could greatly enhance the user experience, especially for those with slower internet connections. Implementing a more detailed legend and tooltips would provide users with better context and understanding of the data being presented. Additionally, incorporating more recent datasets and expanding the map's functionality to include other demographic variables, such as age distribution or educational attainment, could offer a more comprehensive view of King County's demographics. On the 2010 map, although I followed the steps exatcly, the census tract numbers all say undefined for some reason. These improvements would not only enrich the user experience but also provide a deeper and more nuanced understanding of the region's population dynamics.

## Lessons Learned:

Working on this project was a profound learning experience that highlighted the intricacies of data visualization and interactivity. Initially, delving into the King County census data for population statistics revealed the depth and complexity of demographic information. This foundation allowed me to construct a dynamic HTML document, aimed at visualizing three distinct datasets for King County. I discovered the importance of creating an engaging, user-friendly interface, and how the seamless integration of reliable datasets can enhance the viewer's experience. By incorporating interactive features, I realized the power of intuitive design in conveying complex information, ultimately deepening users' understanding of demographic changes over time.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**New Orleans Flood Risk:** [New Orleans Flood Risk Analysis](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/New-Orleans-Flood-Analysis)

**ArcGIS Restaurant Project:** [ArcGIS Fast Food Restaurant Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ArcGIS-Restaurant-Project)

**COVID Cases Map:** [COVID Interactive Cases Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/COVID-Interactive-Maps/COVID%20counts)

**COVID Rates Map:** [COVID Interactive Rates Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/COVID-Interactive-Maps/COVID%20rates)

**Sumner Boundary Map:** [Sumner Boundary Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/Sumner%20Boundary%20Map)

**Lynnwood Right-of-Way:** [Lynnwood Right-of-Way](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/Lynnwood%20Right-of-Way)

**Oso Mudslide:** [Oso Mudslide](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Oso-Mudslide)

**Hurricanes since 1851:** [Hurricanes since 1851](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Hurricanes-since-1851) 

**Miami Sea Level Rise:** [3D Miami Beach Sea Level Rise](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/3D-Miami-Beach-Sea-Level-Rise)

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

## Repositories
**Profile:** https://github.com/T3ch12et

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio


