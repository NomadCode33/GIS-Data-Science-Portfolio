# COVID Cases/Counts Interactive Map
This assignment shows maps that are created from the data sources of COVID-19 regarding the cases. The data is then made into an interactive map to engage the viewer with what is being presented to them.

**Link to project:** https://t3ch12et.github.io/COVID%20Interactive%20Maps/COVID%20counts/

<img src="./COVID Cases Interactive Map.gif" img alt = "COVID Rates GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON, Markdown

To bring this project to life, I began by downloading the necessary datasets from the New York Times, 2018 ACS 5-year estimates, and the U.S. Census Bureau. With the data in hand, I proceeded to develop the HTML file that forms the backbone of the interactive map. Here’s a detailed breakdown of how the HTML code components work together to build the website:

#### Structure and Metadata

1. **DOCTYPE Declaration**:
   - The document begins with `<!DOCTYPE html>`, which specifies that this is an HTML5 document. This declaration ensures that the web browser understands and correctly renders the HTML.

2. **HTML Root Element**:
   - The `<html>` element encloses the entire HTML document, setting up the structure.

#### Head Section

3. **Metadata and Character Set**:
   - `<meta charset="utf-8">` sets the character encoding to UTF-8, which supports a wide range of characters and symbols from different languages.

4. **Page Title**:
   - `<title>US COVID-19 Cases</title>` sets the title that appears in the browser tab, giving users an immediate understanding of the page content.

5. **Viewport Settings**:
   - `<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">` ensures the webpage is responsive across various devices, preventing zooming for a consistent user experience.

6. **External Fonts**:
   - `<link href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap" rel="stylesheet">` links to the Open Sans font from Google Fonts, ensuring a consistent and visually appealing text style throughout the site.

7. **Mapbox GL JS Stylesheet**:
   - `<link href="https://api.mapbox.com/mapbox-gl-js/v2.8.1/mapbox-gl.css" rel="stylesheet">` imports the necessary CSS for the Mapbox GL JS library, which is critical for rendering the interactive map.

8. **Mapbox GL JS Script**:
   - `<script src="https://api.mapbox.com/mapbox-gl-js/v2.8.1/mapbox-gl.js"></script>` links to the Mapbox GL JS library, providing the functionality needed to create the interactive map.

9. **Custom Stylesheet**:
   - `<link rel="stylesheet" href="css/style.css"/>` links to a custom CSS file (`style.css`) for additional styling specific to the webpage, allowing for further customization of the layout and appearance.

#### Body Section

10. **Map Container**:
    - `<div id="map"></div>` creates a `div` element with the ID `map`, serving as the container where the Mapbox map will be rendered.

11. **Legend Container**:
    - `<div id="legend"></div>` creates a `div` element with the ID `legend`, intended to display a legend explaining the map's data visualizations.

12. **Title and Subtitle**:
    - `<div id="title">US COVID-19 Cases</div>` and `<div id="subtitle">December 2020</div>` create `div` elements to display the title and subtitle of the map, providing context and time reference for the data.

13. **Main JavaScript File**:
    - `<script src="js/main.js"></script>` links to an external JavaScript file (`main.js`) where the code to initialize and configure the Mapbox map and add interactive elements is stored.

#### How the Code Works Together

1. **Page Setup**:
   - The `<!DOCTYPE html>` and `<html>` elements define the document's structure, ensuring it is recognized and rendered as an HTML5 document.

2. **Head Section**:
   - The metadata (`<meta>` tags) ensures proper character encoding and responsive design.
   - The linked stylesheets and scripts (`<link>` and `<script>` tags) import external resources required for fonts and Mapbox functionalities, ensuring a consistent and interactive user experience.

3. **Body Section**:
   - The `<div>` elements (`map`, `legend`, `title`, and `subtitle`) structure the page, providing designated areas for the map, legend, title, and subtitle. The `id` attributes allow these elements to be styled and manipulated by CSS and JavaScript.

4. **Map Initialization and Interaction**:
   - The external JavaScript file (`main.js`) contains the code to initialize the Mapbox map within the `map` div. This script sets the map's style, centers it on a specific location, adds data layers, and configures interactive elements such as zoom controls or pop-ups.
   - Additional JavaScript in `main.js` handles the creation and display of the legend and other interactive features, ensuring a dynamic and engaging user experience.

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

## Repositories
**Profile:** [T3ch12et](https://github.com/T3ch12et)

**COVID Map Repository:** [COVID Interactive Maps]()

**Main Repository:** [GIS Data Science Portfolio](https://github.com/T3ch12et/GIS-Data-Science-Portfolio)

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**New Orleans Flood Risk:** [New Orleans Flood Risk Analysis](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/New-Orleans-Flood-Analysis)

**ArcGIS Restaurant Project:** [ArcGIS Fast Food Restaurant Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ArcGIS-Restaurant-Project)

**Lynnwood Right-of-Way:** [Lynnwood Right-of-Way](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/Lynnwood%20Right-of-Way)

**Bothell Bus Base North:** [Bothell Bus Base North](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/Bothell%20Bus%20Base%20North)

**Map of New York:** [Map of New York](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Map-of-New-York)

**Spilhaus Layout:** [Spilhaus Layout Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Spilhaus-Layout)

**Coral Reef Dashboard:** [Coral Reef Dashboard](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Coral-Reef-Dashboard)

**Rondonia Land Cover Change:** [Rondonia Land Cover Change from 1992 to 2020](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Rondonia-Land-Cover-Change)

**Shipping in 1770:** [World Shipping in 1770](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Shipping-in-1770)
