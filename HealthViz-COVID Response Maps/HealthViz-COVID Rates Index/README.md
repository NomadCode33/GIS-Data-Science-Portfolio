# COVID Rates Interactive Map
This assignment shows maps that are created from the data sources of COVID-19 regarding the rates. The data is then made into an interactive map to engage the viewer with what is being presented to them.

**Link to project:** https://t3ch12et.github.io/COVID%20Interactive%20Maps/COVID%20rates/

<img src="./HealthViz-COVID Rates Index.gif" img alt = "COVID Rates GIF"/>

## How It's Made:

**Tech used:** HTML, CSS, JavaScript, GeoJSON, Markdown

To bring this project to life, I embarked on an exciting journey of data exploration and web development. I began by downloading comprehensive datasets from the New York Times, the 2018 ACS 5-year estimates, and the U.S. Census Bureau. With these invaluable datasets at my disposal, I meticulously crafted an HTML document that established the foundation for a dynamic web page, featuring an interactive map that visualizes COVID-19 rates across the United States. Here’s a detailed look at how each part of the HTML works together:

### HTML Document Structure

1. **Starting with the Basics**:
    - The document kicks off with the `<!DOCTYPE html>` declaration, signaling to the browser that it follows the HTML5 standard.
    - The entire structure of the page is wrapped within the `<html>` tag, marking the root of the document.

### Head Section

2. **Setting the Foundation**:
    - Inside the `<head>` section, key meta-information is included.
    - The `<meta charset="utf-8">` tag ensures that the document uses UTF-8 encoding, making sure all characters display correctly.
    - The title of the page, visible on the browser tab, is set using the `<title>Interactive Web Mapping</title>` tag.

3. **Responsive Design and Styling**:
    - The `<meta name="viewport" content="initial-scale=1,maximum-scale=1,user-scalable=no">` tag is crucial for making the webpage responsive, controlling how it scales on different devices.
    - Styling is enhanced by linking to the Mapbox GL JS library’s CSS file with the `<link href="https://api.mapbox.com/mapbox-gl-js/v2.5.0/mapbox-gl.css" rel="stylesheet">`.
    - Additionally, a custom stylesheet (`stylerate.css`) is linked using `<link rel="stylesheet" href="css/stylerate.css"/>`.

4. **Interactive Mapping Power**:
    - The `<script src="https://api.mapbox.com/mapbox-gl-js/v2.5.0/mapbox-gl.js"></script>` tag pulls in the Mapbox GL JS library, enabling the creation of interactive maps.

### Body Section

5. **Bringing the Page to Life**:
    - The `<body>` tag contains the main content of the webpage, where the magic happens.
    - A `<div id="map"></div>` is set up as the map container, acting as the canvas where the Mapbox map will be displayed.
    - Overlays are added with divs like `<div class='map-overlay' id='features'>` and `<div class='map-overlay' id='legend'></div>`, which provide extra layers of information, such as a title, instructions, and a legend.

6. **Interactive Features and Logic**:
    - The `<script src="js/mainrate.js"></script>` tag links to an external JavaScript file that handles the map’s interactivity, from initializing the map to managing user interactions.
    - An empty `<script></script>` tag is also included, ready to house any inline JavaScript that might be added later.

### The Big Picture

- **External Libraries**: By incorporating the Mapbox GL JS library, the document equips itself with powerful tools to build interactive, customizable maps.
- **Styling and Overlays**: The combination of Mapbox’s CSS and the custom `stylerate.css` file ensures that the map and its overlays are visually appealing and easy to use.
- **JavaScript Integration**: The linked JavaScript file (`mainrate.js`) is the engine that drives the map’s functionality, making sure everything runs smoothly and responds to user input.

This HTML document is carefully crafted to create a webpage that displays a dynamic, interactive map powered by Mapbox GL JS. The additional overlays provide users with valuable insights, while the `mainrate.js` file ensures a seamless and engaging user experience.

## Optimizations

The only aspect of the map that could benefit from enhancement is the refinement of data classification. By creating more precise and meaningful categories for the data, the accuracy and clarity of the visualizations would be significantly improved.

## Lessons Learned:

Through the development of this project, I learned how to harness these data sources to create a dynamic web page, featuring an interactive map that visualizes COVID-19 rates across the United States. Constructing the HTML document required meticulous attention to detail, from setting the document type and character encoding to ensuring responsiveness and incorporating essential external libraries for interactive mapping. Crafting the map overlays and integrating custom styles taught me the importance of user-friendly design and clear instructions. By linking the external JavaScript file, I understood how to bring the map to life with seamless interactions. This project not only enhanced my technical skills but also deepened my appreciation for the intricate connections between data, design, and functionality in web development.

## Data Sources
**Link to COVID count cases:** [New York Times](https://github.com/nytimes/covid-19-data/blob/43d32dde2f87bd4dafbb7d23f5d9e878124018b8/live/us-counties.csv).

**Link to COVID rates:** [2018 ACS 5 year estimates](https://data.census.gov/cedsci/table?g=0100000US%24050000&d=ACS%205-Year%20Estimates%20Data%20Profiles&tid=ACSDP5Y2018.DP05&hidePreview=true).

**Link to COVID rates:** [U.S. Census Bureau](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html).

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

**Ship Race from Spain to Puerto Rico:** [Ship Race: Spain to Puerto Rico](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Ship-Race-Spain-to-Puerto-Rico-1770)

**New Orleans Flood Risk:** [New Orleans Flood Risk Analysis](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/New-Orleans-Flood-Analysis)

## Repositories
**Profile:** https://github.com/T3ch12et

**COVID Map Repository:** [COVID Interactive Maps](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/COVID-Interactive-Maps)

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio
