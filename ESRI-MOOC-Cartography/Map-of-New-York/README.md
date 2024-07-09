# Map of New York
Labeled a street map of New York by employing label classes and utilizing queries to target and label specific subsets of features. Additionally, I created an optimized layout for the map, ensuring clear and effective presentation.

<img src="./New York.jpg" img alt = "New York Map"/>

## How It's Made:

**Tech used:** ArcGIS Pro

The project began with a chaotic tangle of labels on a street map of New York, requiring careful organization. My first task was to label the borderline running through the Hudson River between New York and New Jersey. I selected the State Line layer in the Contents pane and activated the labels. Since a single line feature represented the border between the two states, I needed to create distinct labels indicating which side belonged to New York and which to New Jersey.

From the Labeling tab, I navigated to the Label Class group, clicked the Class dropdown arrow, and chose Create Label Class. In the dialog box, I named the new class "Below" for the New York label. The existing class, "Class 1," was renamed to "Above" for the New Jersey label to ensure clarity. I set the class to Above, selected the RIGHT_NAME10 field, and adjusted the text appearance parameters.

Once the Above symbol class was configured, I saved it as a symbol style to apply it to other State Lines classes. In the Label Class pane, under the Symbol tab, I clicked the Menu button and chose Save Symbol to Style, naming it State Line Text Symbol. This symbol appeared in the Text Symbol group on the Labeling tab. I then modified the placement and position settings for the Above label class, saved these settings as State Line Label Placement, and ensured it appeared in the Label Placement group. I switched the Class field to Below, selected the State Line Text Symbol style, and applied the State Line Label Placement. Finally, I adjusted the Constrain Offset placement value to Below Line, resulting in the New Jersey label above and the New York label below the state line feature.

Next, I focused on the MajorRoads feature class, which included various roads like highways and thoroughfares. Using SQL (Structured Query Language) query expressions, I labeled a subset of features, requiring two classes to specify different labeling properties. I turned on the labels for the MajorRoads layer and created two new label classes called Name and Shield. SQL query expressions allowed me to identify a subset of features to label, separating road names and shield numbers for distinct styling. I set the Class to Name and, in the Label Class pane under the Class tab, clicked the SQL Query button. I created a new expression to label features where NameType equaled Name and did the same for the Shield label class with NameType equaled Shield. I then customized the labels for each class according to their respective parameters.

To further refine the map, I configured advanced settings through label weights and label priorities. Label weights allowed me to control which labels were placed when potential conflicts (overlaps) arose between features and labels. I selected the Place layer, then, from the Labeling tab in the Map group, clicked More and chose Weights. For the Place - Class 1 label class, I ensured the Feature Weight was set to 1000. With the Place layer selected, I went to the Map group on the Labeling tab, clicked More, and chose Properties. In the Label Priority Ranking window, I moved MajorRoads - Shield above MajorRoads - Name and positioned both above Road. Finally, I added the necessary elements for the Layout tab of the map and exported the completed project.

This meticulous process transformed a cluttered map into an organized, visually appealing, and informative street map of New York. Through this project, I learned to leverage advanced GIS tools and techniques to create clear, well-designed maps that effectively communicate essential information.

## Lessons Learned:

This project taught me several valuable lessons in map organization, label management, and the use of advanced GIS tools. I began by transforming a cluttered street map of New York into an organized and visually appealing representation. Labeling the borderline along the Hudson River between New York and New Jersey required creating distinct labels for each state, which I accomplished by carefully setting up label classes and configuring their appearance and placement. 

Through the process, I learned the importance of using SQL query expressions to label subsets of features, such as differentiating road names and shield numbers within the MajorRoads feature class. This exercise highlighted the power of data-driven symbology and precise label management to enhance map readability. 

I also discovered the significance of label weights and priorities in resolving potential conflicts and ensuring that the most important information is clearly displayed. By fine-tuning these settings, I could control the placement of overlapping labels effectively. 

Overall, this project deepened my understanding of the principles of visual hierarchy and effective map design. It demonstrated how thoughtful organization and the strategic use of GIS tools can turn a chaotic dataset into a clear and informative map, showcasing my ability to create compelling and accurate visual representations.

## Repositories
**Profile:** [T3ch12et](https://github.com/T3ch12et)

**Cartography Repository:** [ESRI MOOC Cartography](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography)

**Main Repository:** [GIS Data Science Portfolio](https://github.com/T3ch12et/GIS-Data-Science-Portfolio)

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Miami Sea Level Rise:** [3D Miami Beach Sea Level Rise](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/3D-Miami-Beach-Sea-Level-Rise)

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

**Oso Mudslide:** [Oso Mudslide](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Oso-Mudslide)

**Hurricanes since 1851:** [Hurricanes since 1851](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Hurricanes-since-1851) 

**Coral Reef Dashboard:** [Coral Reef Dashboard](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Coral-Reef-Dashboard)

**Rondonia Land Cover Change:** [Rondonia Land Cover Change from 1992 to 2020](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Rondonia-Land-Cover-Change)

**Addressing Climate Change:** [Using GIS to address climate change](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/blob/main/ESRI-MOOC-GIS-for-Climate-Action/Addressing-Climate-Change/README.md)

**Shipping in 1770:** [World Shipping in 1770](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Shipping-in-1770)

**Ship Race from Spain to Puerto Rico:** [Ship Race: Spain to Puerto Rico](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Ship-Race-Spain-to-Puerto-Rico-1770)

**Map of Massachusetts:** [Map of Massachusetts](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Map-of-Massachusetts)
