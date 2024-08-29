# City of Miami Beach Sea Level Rise
A dynamic 3D map highlighting the buildings in Miami, Florida that are projected to be at risk from rising sea levels by 2050.

<img alt = "Sea Level Rise GIF" img src="./ArcGIS - City of Miami Beach Sea Level Rise_EmekaEmeche (3).gif"/>

## How It's Made:

**Tech used:** ArcGIS Pro, ArcGIS Online, ArcGIS Living Atlas of the World, ArcGIS 3D Analyst extension

I started by downloading Miami’s dataset and transforming a flat 2D map into a dynamic 3D display. My first task was setting the building extrusions, as all the buildings initially appeared at the same height. To correct this, I used the join field tool to merge tables and accurately assign real-world building heights. I then created multipatch layers to add depth, using the symbology pane and a rule package file (RPK) to add detailed textures, windows, and realistic roof shapes. For a natural touch, I added water data, adjusting the symbology to create a realistic water appearance and setting the lighting to match the morning sun at 8 AM.

With the city’s foundation set, I shifted to gathering sea level rise data from the ArcGIS Living Atlas of the World, focusing on NOAA's intermediate-high projections for 2030, 2050, and 2090. I processed these layers using the Environments Geoprocessing tool and converted them into interactive polygons with the raster to polygon tool.

Next, I assessed which buildings would be affected by future sea level rise. Using the Select by Location tool, I filtered the building layer based on the 2030, 2050, and 2090 projections. In the attribute table, I added a new column, "Inundated_Year," to mark the year each building could be at risk. I then applied color coding in the symbology pane to highlight risk levels: green for unaffected, light orange for 2030, dark orange for 2050, and red for 2090.

To dive deeper, I used the Elevation Profile tool to measure building heights, revealing that those not at risk were constructed on higher ground, demonstrating the critical need to consider sea level rise in future developments.

Finally, I uploaded the completed 3D map to ArcGIS Online, making it accessible for public exploration and understanding.

## Optimizations

To enhance this project, incorporating a web app would be highly beneficial. This web app would allow the community and decision-makers in Miami Beach to interact with the analysis results and visualize the impact of rising sea levels over time. By providing an accessible and user-friendly platform, stakeholders can better understand the data, explore different scenarios, and make informed decisions to address the challenges posed by sea level rise.

## Lessons Learned:

I never would have imagined I could create a map like this; it was definitely a rewarding learning experience. Throughout the process of developing this 3D map, I was thrilled to see it improve over time. I mastered valuable tools such as the environments geoprocessing tool, raster to polygon conversion, and the use of RPK files, among others. The end result was impressive, and I gained a deeper understanding of the many ways GIS can be used to convey complex topics. With this newfound knowledge, I am now equipped to create more detailed and impactful 3D maps to address various global issues.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

**Oso Mudslide:** [Oso Mudslide](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Oso-Mudslide)

**West Seattle Light Rail Survey:** [West Seattle Light Rail Survey](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/West%20Seattle%20Light%20Rail%20Survey)

## Repositories
**Profile:** https://github.com/T3ch12et

**GIS Climate Action Repository:** [ESRI MOOC GIS for Climate Action](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action)

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio
