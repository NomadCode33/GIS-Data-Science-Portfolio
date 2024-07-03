# City of Miami Beach Sea Level Rise
A dynamic 3D map highlighting the buildings in Miami, Florida that are projected to be at risk from rising sea levels by 2050.

<img alt = "Sea Level Rise GIF" img src="./ArcGIS - City of Miami Beach Sea Level Rise_EmekaEmeche (3).gif"/>

## How It's Made:

**Tech used:** ArcGIS Pro, ArcGIS Online, ArcGIS Living Atlas of the World, ArcGIS 3D Analyst extension

I began by downloading the dataset of Miami and transforming the 2D map into a 3D display. The next step was to set the extrusion of the buildings. After the extrusion, I used the join field tool to merge tables, transferring attributes to accurately reflect the varied building heights, as initially, all buildings were the same size. To further align the buildings with their real-life counterparts, I created multipatch layers. Utilizing the symbology pane and a rule package file (RPK), I enhanced the buildings with detailed textures and windows, and the RPK file also modified the roof shapes for realism. I then added water data, creating a realistic 3D representation through the symbology pane, and set the illumination to reflect 8 AM lighting conditions.

With the basics completed, I focused on acquiring sea level rise data from the ArcGIS Living Atlas of the World, specifically layers for intermediate-high sea level rise projections for 2030, 2050, and 2090 from NOAA's Digital Coast. I used the Environments Geoprocessing tool to configure this data, and the raster to polygon tool to convert the data into polygons for better interactivity. 

Next, I calculated the affected buildings by filtering the building layer using the Select by Location tool with the sea level rise data for 2030, 2050, and 2090. In the attribute table, I created a new column called "Inundated_Year" to indicate the year each building is at risk. Using the symbology pane, I assigned unique colors to reflect the risk levels: green for not affected, light-orange for 2030, dark-orange for 2050, and red for 2090. 

To further analyze, I used the Elevation Profile tool to measure the elevation of buildings, finding that those not at risk were built at higher elevations with sea level rise in mind, unlike the vulnerable buildings. This insight emphasizes the importance of considering sea level rise in future building developments.

Finally, I uploaded the 3D map onto ArcGIS Online for public viewing.

## Optimizations

To enhance this project, incorporating a web app would be highly beneficial. This web app would allow the community and decision-makers in Miami Beach to interact with the analysis results and visualize the impact of rising sea levels over time. By providing an accessible and user-friendly platform, stakeholders can better understand the data, explore different scenarios, and make informed decisions to address the challenges posed by sea level rise.

## Lessons Learned:

I never would have imagined I could create a map like this; it was definitely a rewarding learning experience. Throughout the process of developing this 3D map, I was thrilled to see it improve over time. I mastered valuable tools such as the environments geoprocessing tool, raster to polygon conversion, and the use of RPK files, among others. The end result was impressive, and I gained a deeper understanding of the many ways GIS can be used to convey complex topics. With this newfound knowledge, I am now equipped to create more detailed and impactful 3D maps to address various global issues.

## Repositories
**GIS Climate Action Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action <br>
**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Athens Heat Risk Index:** https://github.com/T3ch12et/Athens-Heat-Risk-Index/tree/main <br>
**Oso Mudslide:** https://github.com/T3ch12et/Oso-Mudslide/tree/main <br>
**Hurricanes since 1851:** https://github.com/T3ch12et/Hurricanes-since-1851
