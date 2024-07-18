# COVID Rates Interactive Map
This assignment shows maps that are created from the data sources of COVID-19 regarding the rates. The data is then made into an interactive map to engage the viewer with what is being presented to them.

**Link to project:** https://t3ch12et.github.io/COVID%20Interactive%20Maps/COVID%20rates/

<img src="./COVID Rates Interactive Map.gif" img alt = "COVID Rates GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON, Markdown

To bring this project to life, I embarked on an exciting journey of data exploration and web development. I began by downloading comprehensive datasets from the New York Times, the 2018 ACS 5-year estimates, and the U.S. Census Bureau. With these invaluable datasets at my disposal, I meticulously crafted an HTML document that established the foundation for a dynamic web page, featuring an interactive map that visualizes COVID-19 rates across the United States. Here’s a detailed look at how each part of the HTML works together:

### HTML Document Structure

1. **`<!DOCTYPE html>`**:
    - This declaration informs the browser that the document adheres to the HTML5 standard.

2. **`<html>`**:
    - The root element that encapsulates the entire HTML document.

### Head Section

3. **`<head>`**:
    - Contains meta-information essential for the document.

4. **`<meta charset="utf-8">`**:
    - Defines the character encoding for the document as UTF-8, ensuring proper display of text.

5. **`<title>Interactive Web Mapping</title>`**:
    - Sets the title of the webpage, visible on the browser tab.

6. **`<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">`**:
    - Configures the viewport for responsive design, setting initial and maximum zoom levels while disabling user scaling.

7. **`<link href="https://api.mapbox.com/mapbox-gl-js/v2.5.0/mapbox-gl.css" rel="stylesheet">`**:
    - Links to the CSS file from the Mapbox GL JS library, providing essential styles for the map.

8. **`<script src="https://api.mapbox.com/mapbox-gl-js/v2.5.0/mapbox-gl.js"></script>`**:
    - Incorporates the Mapbox GL JS library’s JavaScript, enabling the interactive mapping capabilities.

9. **`<link rel="stylesheet" href="css/stylerate.css"/>`**:
    - Links to an external CSS file (`stylerate.css`) for additional custom styles.

### Body Section

10. **`<body>`**:
    - The main content area of the webpage.

11. **`<div id="map"></div>`**:
    - A div element designated to host the Mapbox map.

12. **`<div class='map-overlay' id='features'>`**:
    - An overlay div for displaying features on the map, particularly information about US COVID rates.
    - **`<h2>US COVID Rates</h2>`**: A prominent heading for the overlay.
    - **`<div id='text-description'><p>Hover over a state!</p></div>`**: Instructions for users to interact with the map.

13. **`<div class='map-overlay' id='legend'></div>`**:
    - A reserved div for displaying the map’s legend, explaining data visualizations.

14. **`<script src="js/mainrate.js"></script>`**:
    - Links to an external JavaScript file (`mainrate.js`), likely containing the logic for initializing and managing the interactive map.

15. **`<script></script>`**:
    - An empty script tag, ready for additional inline JavaScript if necessary.

### Bringing It All Together

- **External Libraries**: By importing the Mapbox GL JS library, we enable the creation of highly interactive, customizable maps.
- **Styling**: The combined power of the Mapbox CSS and our custom `stylerate.css` file ensures the map and overlays are visually appealing and user-friendly.
- **Map Container**: The `div` with the `id="map"` acts as the canvas where the Mapbox map is rendered.
- **Overlays**: The `map-overlay` divs serve as additional layers providing contextual information, such as titles, instructions, and legends.
- **JavaScript Logic**: The external JavaScript file (`mainrate.js`) is the brain behind the map’s functionality, initializing the map, adding data layers, handling user interactions, and updating the overlays dynamically.

This HTML document meticulously constructs a web page framework, integrating necessary libraries and components to display an interactive map powered by Mapbox GL JS. The additional overlays enrich the user experience, presenting valuable information about US COVID rates. The `mainrate.js` file plays a crucial role in bringing the map to life, ensuring it responds seamlessly to user interactions.

## Optimizations

The only aspect of the map that could benefit from enhancement is the refinement of data classification. By creating more precise and meaningful categories for the data, the accuracy and clarity of the visualizations would be significantly improved.

## Lessons Learned:

Through the development of this project, I learned how to harness these data sources to create a dynamic web page, featuring an interactive map that visualizes COVID-19 rates across the United States. Constructing the HTML document required meticulous attention to detail, from setting the document type and character encoding to ensuring responsiveness and incorporating essential external libraries for interactive mapping. Crafting the map overlays and integrating custom styles taught me the importance of user-friendly design and clear instructions. By linking the external JavaScript file, I understood how to bring the map to life with seamless interactions. This project not only enhanced my technical skills but also deepened my appreciation for the intricate connections between data, design, and functionality in web development.

## Data Sources
**Link to COVID count cases:** [New York Times](https://github.com/nytimes/covid-19-data/blob/43d32dde2f87bd4dafbb7d23f5d9e878124018b8/live/us-counties.csv).

**Link to COVID rates:** [2018 ACS 5 year estimates](https://data.census.gov/cedsci/table?g=0100000US%24050000&d=ACS%205-Year%20Estimates%20Data%20Profiles&tid=ACSDP5Y2018.DP05&hidePreview=true).

**Link to COVID rates:** [U.S. Census Bureau](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html).

## Repositories
**Profile:** [T3ch12et](https://github.com/T3ch12et)

**COVID Map Repository:** [COVID Interactive Maps](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/COVID-Interactive-Maps)

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
