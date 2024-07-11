# Coral Reef Dashboard
An interactive dashboard displaying coral reef pollution and health at local, regional, and global scales.

<img alt = "Coral Reef Dashboard GIF" img src="./Coral Reef Bleaching Dashboard_EmekaEmeche (1).gif"/>

## How It's Made:

**Tech used:** ArcGIS Online, ArcGIS Dashboards

Accessing ArcGIS Online, I began my project by searching for NOAA Coral Reef Watch data. Opening it in Map Viewer, I prepared the web map for the dashboard, meticulously examining all layers and features. The attribute table displayed critical information, such as Degree Heating Weeks and Alert Level, which would be central to my dashboard. Choosing the Human Geography Dark Map from the Basemap options, I zoomed in to fill the map view. After saving the map and inputting the necessary information, I moved on to creating a new dashboard, selecting a dark theme, and updating the header with the dashboard's title.

I then added list elements to display the monitoring status at each virtual station, sorting them by the highest accumulated heat stress. Clicking "Add Element" and selecting "List," I positioned it on the left side of the dashboard. Linking the layers from my Coral Reef Bleaching web map, I expanded the NOAA Coral Reef Watch (CRW) Virtual Stations layer. Sorting the Degree Heating Weeks in descending order, I updated the list text to dynamically display the monitoring status at each virtual station.

On the Actions tab, I enabled the "Show Pop-Up" option for the Coral Reef Bleaching feature to display pop-ups when a location was selected. I added a serial chart to show the number of virtual stations by alert level, ranging from 0 (no bleaching) to 4 (severe bleaching). Placing the chart on the left side of the dashboard, I sourced the layer from the Coral Reef Bleaching web map and expanded the NOAA Coral Reef Watch (CRW) Virtual Stations layer. In the Data Options pane, I selected "Alert Level" for the Category Field, adjusted the x-axis labels in the Category Axis tab, and changed the y-axis label to "Number of Coral Stations" in the Value Axis tab. In the Series tab, I chose "By Category" for the Bar Color option, assigning colors to represent coral bleaching severity: light blue for No Alert, light yellow for Watch, peach for Warning, light brown for Level 1, and dark brown for Level 2. To ensure the actions worked, the elements had to share a data source or be mapped to the data source. I filtered the Target Field to "Alert Level" in the Actions tab, so clicking on the bar graph for an alert level would show the corresponding points on the map.

Finally, I added an indicator element to the top left corner of the map to display dynamic summary statistics based on attribute fields in the dashboard data. This indicator reported the number of virtual stations at risk of bleaching. Selecting the Coral Reef Bleaching web map from the Virtual Stations layer of NOAA Coral Reef Watch (CRW), I built an expression filter stating _Alert Level Greater Than Or Equal 3_ to show the number of stations with a Level 1 or 2 alert. I included the total count of virtual stations for context, choosing "Statistic" for the Reference type. In the Indicator Options pane, I typed "Coral reefs at risk of bleaching" out of the total number of stations. Lastly, I configured the actions to ensure the different elements of the dashboard interacted seamlessly.

## Lessons Learned:

I discovered how to source web maps from ArcGIS Online into ArcGIS Dashboards to create dynamic and interactive maps. By isolating specific layers, I ensured they were prominently displayed on the dashboard I was creating. Utilizing data points from these layers allowed the pop-ups to convey meaningful information, enhancing the viewing experience and inspiring people to take action. 

With a variety of customization options at my disposal, I could design a stylish and personalized layout on Dashboards. I was thrilled by the process and amazed at how even small actions could culminate in a tool that could help many people and drive societal change. The versatility of GIS continuously astonishes me, given its straightforward premise of creating maps for others to use.

Witnessing the interactivity between different apps on ArcGIS coming together to create fantastic products was both fascinating and gratifying. It’s incredible to see how these tools can seamlessly integrate to produce something impactful and beneficial.

## Repositories
**Profile:** [T3ch12et](https://github.com/T3ch12et)

**GIS Climate Action Repository:** [ESRI MOOC GIS for Climate Action](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action)

**Main Repository:** [GIS Data Science Portfolio](https://github.com/T3ch12et/GIS-Data-Science-Portfolio)

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Miami Sea Level Rise:** [3D Miami Beach Sea Level Rise](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/3D-Miami-Beach-Sea-Level-Rise)

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

**Oso Mudslide:** [Oso Mudslide](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Oso-Mudslide)

**Hurricanes since 1851:** [Hurricanes since 1851](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Hurricanes-since-1851)

**Rondonia Land Cover Change:** [Rondonia Land Cover Change from 1992 to 2020](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Rondonia-Land-Cover-Change)

**Addressing Climate Change:** [Using GIS to address climate change](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/blob/main/ESRI-MOOC-GIS-for-Climate-Action/Addressing-Climate-Change/README.md)
