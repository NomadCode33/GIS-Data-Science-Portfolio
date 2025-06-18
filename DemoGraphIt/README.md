# DemoGraphIt: Interactive Census Mapping Tool
An interactive HTML map built using King County census data, featuring three datasets: population data from 2000 and 2010, and poverty data from 2012–2016. Designed to enhance user experience, the map allows viewers to toggle between datasets using intuitive buttons, offering clear, reliable, and accessible visualizations for demographic analysis and decision-making.

**Link to project:** https://nomadcode33.github.io/DemoGraphIt/

<img src="./DemoGraphIt.gif" img alt = "Population GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON

The project embarked on an intriguing journey with the retrieval of King County census data, focusing on the population statistics. This initial step allowed me to delve into the dataset, laying the groundwork for constructing an interactive HTML document. The objective was clear: to create a dynamic map showcasing three distinct datasets for King County. These datasets included the census tract population for the years 2000 and 2010, and a poverty map for the same region.

To achieve this, I incorporated a button feature that effortlessly switches between the different datasets, enhancing the viewer's experience by providing a seamless transition between the maps. The use of reliable and esteemed datasets was paramount, ensuring the accuracy and credibility of the visualizations. My goal was to create an engaging, user-friendly interface that allowed users to interact with the data intuitively, thus gaining a deeper understanding of the demographic changes over the years.

The HTML document was crafted like the foundation of a story, carefully laying out each element to bring an interactive map to life.

### 1. **Setting the Stage: HTML Structure**
   - The story begins with the `<!DOCTYPE html>` declaration, setting the stage for an HTML5-compliant document. The main characters, `<html>`, `<head>`, and `<body>`, were introduced, forming the backbone of the page.
   - Within the `<head>` section, a title was bestowed upon the document, and a link to the Leaflet CSS file was established to style the upcoming map. Here, the external elements were gathered, much like tools for a grand adventure.
   - The `<body>` was then prepared, housing scripts that included Leaflet, a powerful map-making library, along with jQuery for handling the AJAX requests needed to retrieve data from a GeoJSON file named `KCPop2000.js`.

### 2. **Bringing the Map to Life: Leaflet Initialization**
   - The journey continued as a `<div>` with the ID `mapid` was created to serve as the canvas for the map. Its dimensions were carefully defined (800px by 600px) and centered using CSS, ensuring the map would take center stage.
   - With this canvas in place, the Leaflet map, dubbed `mymap`, was brought to life. Its heart was set to beat in the coordinates of Seattle (latitude: 47.6062, longitude: -122.3321) with a zoom level of 10, setting the scene for an expansive view.
   - To enrich this view, a tile layer from OpenStreetMap was added, draping the map in detailed, familiar base tiles.

### 3. **Defining the World: Styling and Classification**
   - As the story deepened, functions such as `popStyle`, `classification`, `newStyle`, and `oldStyle` were crafted to give meaning and color to the population data from 2000.
   - The `classification` function categorized the population data, assigning colors to each range like a painter filling in a canvas. These hues offered clear visual distinctions, making the story’s world vibrant and understandable.
   - The `newStyle` and `oldStyle` functions added a touch of magic, with mouse hover effects that highlighted boundaries, making the world interactive and responsive to the user's touch.

### 4. **Revealing the Secrets: Popup Functions**
   - Like the unveiling of secrets, the `popUp2000` and `popUp2010` functions were scripted to bind popups to map layers. These popups revealed census tract names and population data from 2000 and 2010, respectively.
   - These functions also controlled the choreography of mouse events—showing and hiding popups and altering styles on hover—providing a dynamic, engaging experience as users explored the map.

### 5. **Exploring Deeper Layers: Poverty Data**
   - The story then delved into the more intricate layers of poverty data, where functions like `povStyle` and `povclass` were penned to style data based on percentage ranges, revealing the socioeconomic contours of the map.
   - The `povUp200` function played a key role in bringing these layers to the surface, binding popups that displayed poverty data for each census tract, with interactions that mirrored those of the population functions.

### 6. **Building the Narrative: GeoJSON Data Layers**
   - The narrative was enriched with the creation of three GeoJSON layers: `pop2000Layer` for 2000’s population data, `pop2010Layer` for 2010, and `povper200Layer` for poverty percentages.
   - Like gathering chapters, data for `pop2010Layer` and `povper200Layer` was loaded asynchronously using jQuery’s `$.getJSON` method, ensuring that the story unfolded smoothly without interruption.

### 7. **Guiding the Reader: Layer Control**
   - To keep the story clear and focused, functions like `pop2000`, `pop2010`, and `povper200` were written. These functions allowed users to add or remove the corresponding data layers, ensuring that only one layer was visible at a time, much like turning pages to focus on one chapter at a time.

### 8. **Empowering the Explorer: Control Buttons**
   - Finally, three buttons were created, each corresponding to a different data layer. These buttons were the keys to exploring the different facets of the map. With a simple click, users could toggle between datasets, seamlessly moving between different parts of the story.

This tale, meticulously written in code, leveraged Leaflet and GeoJSON to create a rich, interactive map that vividly visualized King County’s demographic data. Users could easily switch between various datasets, offering them a comprehensive tool to explore and understand the evolving narrative of demographic shifts and economic conditions over time.

## Optimizations

Exploring the website, several optimizations stand out that significantly enhanced the project's functionality and user experience. The seamless integration of Leaflet and GeoJSON provided a robust framework for interactive mapping, ensuring smooth and responsive map interactions. The implementation of intuitive buttons to switch between different datasets allowed users to easily navigate through various data layers, providing a clear and comprehensive view of King County's demographic changes. The thoughtful use of color classification and hover effects brought the data to life, making it visually appealing and easier to interpret. These optimizations collectively created an engaging and informative tool that effectively communicated complex demographic information.

While the project already excels in many areas, there are still opportunities for further enhancement. Improving the loading speed of the map layers could greatly enhance the user experience, especially for those with slower internet connections. Implementing a more detailed legend and tooltips would provide users with better context and understanding of the data being presented. Additionally, incorporating more recent datasets and expanding the map's functionality to include other demographic variables, such as age distribution or educational attainment, could offer a more comprehensive view of King County's demographics. On the 2010 map, despite meticulously following all the steps, the census tract numbers are all displaying as undefined for some reason. These improvements would not only enrich the user experience but also provide a deeper and more nuanced understanding of the region's population dynamics.

## Lessons Learned:

Working on this project was a profound learning experience that highlighted the intricacies of data visualization and interactivity. Initially, delving into the King County census data for population statistics revealed the depth and complexity of demographic information. This foundation allowed me to construct a dynamic HTML document, aimed at visualizing three distinct datasets for King County. I discovered the importance of creating an engaging, user-friendly interface, and how the seamless integration of reliable datasets can enhance the viewer's experience. By incorporating interactive features, I realized the power of intuitive design in conveying complex information, ultimately deepening users' understanding of demographic changes over time.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Lynnwood Right-of-Way:** [Lynnwood ROW Acquisition](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Lynnwood%20ROW%20Acquisition)

**EcoPulse Web App:** [EcoPulse Climate Interactive Web App](https://github.com/NomadCode33/NomadGeo/tree/main/EcoPulse/EcoPulse%20Climate%20Interactive%20Web%20App)

**EcoPulse Report:** [EcoPulse Climate Analysis Report](https://github.com/NomadCode33/NomadGeo/tree/main/EcoPulse/EcoPulse%20Climate%20Analysis%20Report)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)

