# COVID Cases/Counts Interactive Map
This assignment shows maps that are created from the data sources of COVID-19 regarding the cases. The data is then made into an interactive map to engage the viewer with what is being presented to them.

**Link to project:** https://t3ch12et.github.io/COVID%20Interactive%20Maps/COVID%20counts/

<img src="./COVID Cases Interactive Map.gif" img alt = "COVID Rates GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON, Markdown

To bring this project to life, I began by downloading the necessary datasets from the New York Times, 2018 ACS 5-year estimates, and the U.S. Census Bureau. With the data in hand, I proceeded to develop the HTML file that forms the backbone of the interactive map. Here’s a detailed breakdown of how the HTML code components work together to build the website:

### Building an Engaging Interactive Map

The project began with a foundational HTML document, carefully constructed to support the dynamic visualization of COVID-19 cases across the U.S. The structure unfolded step by step, each component playing a critical role in bringing the interactive map to life.

#### Setting Up the HTML Framework

It all started with the `<!DOCTYPE html>` declaration, a vital command that signals to browsers that this is an HTML5 document. This was followed by the opening `<html>` tag, which wrapped the entire structure, creating the backbone of the page.

Inside the `<head>` section, I laid out the essentials. The `<meta charset="utf-8">` tag ensured that the document used UTF-8 encoding, supporting a wide range of characters and symbols from various languages. The `<title>` tag defined "US COVID-19 Cases" as the page’s title, clearly indicating the content to users right from their browser tabs. To make sure the page looked great on all devices, I added a `<meta>` tag for viewport settings to ensure a responsive design.

External resources were linked next. The Google Font "Open Sans" was imported to establish a clean and consistent text style throughout the site. Then came the stylesheet for Mapbox GL JS, crucial for rendering the interactive map, and the corresponding JavaScript library, both of which were linked to bring the interactive mapping functionality to the page. To further customize the look and feel, a custom stylesheet, `style.css`, was added.

#### Creating the Interactive Map Area

With the framework established, it was time to build the body of the page, where the actual map would come to life. I started by defining a `<div>` with the ID `map`, which served as a container for the Mapbox map. Adjacent to it, another `<div>` with the ID `legend` was created, ready to display a legend explaining the various data visualizations on the map.

To add context and clarity to the map, I created `<div>` elements for the title and subtitle—“US COVID-19 Cases” and “December 2020”—providing users with immediate insight into the data being presented.

Finally, I linked the `main.js` JavaScript file, where all the interactive map functionalities would be scripted. This included the code to initialize and configure the Mapbox map, manage data layers, and create dynamic elements like pop-ups and zoom controls.

#### Bringing Everything Together: How the Code Works

The setup process began with the document’s structure, clearly defined by the `<!DOCTYPE html>` declaration and wrapped within the `<html>` element. This ensured the page was interpreted correctly by the browser as an HTML5 document.

Within the `<head>`, essential metadata tags controlled character encoding and ensured the design was responsive. The linked stylesheets and scripts brought in external resources for consistent typography and the interactive map functionality provided by Mapbox.

In the `<body>`, the strategically placed `<div>` elements—`map`, `legend`, `title`, and `subtitle`—structured the page, designating specific areas for each component. These elements could then be styled and manipulated using CSS and JavaScript.

The `main.js` file played a pivotal role in initializing the map within the `map` div. It set the map’s style, centered it on a specific location, added data layers, and configured interactive elements like zoom controls and pop-ups. The JavaScript also handled the creation and display of the legend, ensuring a dynamic and engaging user experience.

### Final Touches: Animation and Interaction

To make the data more engaging, the JavaScript included in `main.js` managed the animation and interaction elements. It dynamically updated the map’s content, highlighting changes over time and providing users with an intuitive way to explore the data.

By the end of this meticulous process, the webpage transformed into a vivid, interactive tool that allowed users to delve deep into the data on COVID-19 cases across the United States. The combination of thoughtful structuring, strategic use of external libraries, and careful coding created a seamless, informative, and visually appealing experience, bringing complex data to life in a way that was both accessible and engaging.

#### Example `main.js` Code Explanation

Here’s an example of what the `main.js` file might contain to bring the map to life:

```javascript
mapboxgl.accessToken = 'your-access-token'; // Your Mapbox access token

const map = new mapboxgl.Map({
    container: 'map', // ID of the container element
    style: 'mapbox://styles/mapbox/streets-v11', // Map style
    center: [-98.5795, 39.8283], // Initial map center [longitude, latitude]
    zoom: 4 // Initial zoom level
});

map.on('load', function() {
    // Add a source and layer for COVID-19 cases
    map.addSource('covid-cases', {
        type: 'geojson',
        data: 'path/to/your/covid-cases-data.geojson'
    });

    map.addLayer({
        id: 'covid-cases-layer',
        type: 'circle',
        source: 'covid-cases',
        paint: {
            'circle-color': '#f28cb1',
            'circle-radius': 5
        }
    });
});

// Additional code for interactivity, legend, etc.
```
This HTML document sets up the structure of the webpage, links necessary stylesheets and scripts, and provides placeholders for the map, legend, title, and subtitle. The JavaScript in `main.js` uses the Mapbox GL JS library to render and configure the map, adding data and interactivity to create an informative and engaging visualization of US COVID-19 cases. Through careful planning and execution, this project seamlessly integrates data, design, and functionality to deliver a compelling user experience.

## Optimizations

To bring the project to life, I started by setting up the HTML document with `<!DOCTYPE html>` and the `<html>` tag, ensuring it's recognized as an HTML5 document. The `<head>` section was crafted to include essential metadata for character encoding and responsive design, while linked stylesheets and scripts incorporated external resources for fonts and Mapbox functionalities, guaranteeing a seamless and interactive user experience.

In the `<body>`, I used `<div>` elements to neatly organize the page into areas for the map, legend, title, and subtitle. This careful structuring allowed for a clear and intuitive layout. The external JavaScript file played a crucial role, initializing the Mapbox map, adding data layers, and configuring interactive elements to create a dynamic and engaging visualization.

While the map was robust, I identified areas for improvement. For instance, the large dots in the legend could cause confusion. To enhance clarity, increasing the number of data classes would have allowed for better differentiation and a more refined presentation.

## Lessons Learned:

Working on this project was an enlightening journey that taught me invaluable lessons about data integration, web development, and user experience. Starting with downloading datasets from reputable sources like the New York Times and the U.S. Census Bureau, I meticulously crafted an HTML file to underpin the interactive map. I learned the importance of proper document structure, metadata for character encoding, and responsive design to ensure accessibility across devices. Integrating external resources, such as fonts and the Mapbox library, highlighted the necessity of harmonizing design and functionality. By organizing the webpage with well-defined elements for the map, legend, title, and subtitle, I grasped how crucial clear, intuitive layouts are for effective data presentation. The project's culmination, a dynamic visualization of US COVID-19 cases, underscored the power of combining careful planning with advanced tools to create an engaging user experience.

## Data Sources
**Link to COVID count cases:** [New York Times](https://github.com/nytimes/covid-19-data/blob/43d32dde2f87bd4dafbb7d23f5d9e878124018b8/live/us-counties.csv).

**Link to COVID rates:** [2018 ACS 5 year estimates](https://data.census.gov/cedsci/table?g=0100000US%24050000&d=ACS%205-Year%20Estimates%20Data%20Profiles&tid=ACSDP5Y2018.DP05&hidePreview=true).

**Link to COVID rates:** [U.S. Census Bureau](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html).

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Rondonia Land Cover Change:** [Rondonia Land Cover Change from 1992 to 2020](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Rondonia-Land-Cover-Change)

**Ship Race from Spain to Puerto Rico:** [Ship Race: Spain to Puerto Rico](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Ship-Race-Spain-to-Puerto-Rico-1770)

**Population Map:** [Population Interactive Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Population-Interactive-Map)

## Repositories
**Profile:** https://github.com/T3ch12et

**COVID Map Repository:** [COVID Interactive Maps](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/COVID-Interactive-Maps)

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio
