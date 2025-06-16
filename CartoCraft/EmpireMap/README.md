# EmpireMap: New York in Layers
Labeled a street map of New York by employing label classes and utilizing queries to target and label specific subsets of features. Additionally, I created an optimized layout for the map, ensuring clear and effective presentation.

<img src="./New York.jpg" img alt = "New York Map"/>

## How It's Made:

**Tech used:** ArcGIS Pro

The project began with a chaotic mess of labels on a street map of New York, where text cluttered the Hudson River and overlapped streets, making the map hard to read. My mission was to bring clarity to this tangle, starting with the line that ran down the middle of the Hudson River, marking the border between New York and New Jersey.

I selected the State Line layer in the Contents pane and activated the labels. Since one line represented the border between the two states, I needed to create distinct labels to clearly indicate which side belonged to New York and which to New Jersey. 

From the Labeling tab, I went to the Label Class group, clicked on the Class dropdown arrow, and chose to create a new label class. I named the new class "Below" to represent the New York label, while the existing class, "Class 1," was renamed "Above" for New Jersey. This clear naming helped keep things organized. I set the "Above" class to use the RIGHT_NAME10 field, adjusting the text appearance settings to make sure the labels were legible.

Once the “Above” symbol class was set, I saved it as a symbol style to apply to other State Lines classes. In the Label Class pane under the Symbol tab, I clicked the menu button, chose "Save Symbol to Style," and named it "State Line Text Symbol." This symbol now appeared in the Text Symbol group on the Labeling tab. I adjusted the placement and position settings for the "Above" label class, saved these as "State Line Label Placement," and ensured they appeared in the Label Placement group. I then switched the Class field to "Below," selected the "State Line Text Symbol" style, and applied the "State Line Label Placement." I adjusted the Constrain Offset placement value to "Below Line," resulting in the New Jersey label appearing above and the New York label below the state line feature. 

Next, I moved on to the MajorRoads feature class, which included highways and major thoroughfares. I needed to use SQL (Structured Query Language) query expressions to create two different label classes: one for road names and another for road shields, like highway signs. I turned on the labels for the MajorRoads layer and created two new label classes called "Name" and "Shield." Using SQL query expressions, I identified a subset of features to label separately, defining which attributes would apply to the road names and which to the shield numbers. For the "Name" class, I used an expression where NameType equaled “Name,” and for the "Shield" class, I used an expression where NameType equaled “Shield.” This allowed me to give each class its own styling, enhancing their distinction on the map.

To refine the map further, I adjusted advanced settings using label weights and label priorities. Label weights helped control which labels appeared when there were overlaps, ensuring the most critical information was visible. I selected the Place layer, and from the Labeling tab, chose "Weights" under the More options. For the Place - Class 1 label class, I set the Feature Weight to 1000, prioritizing these labels. In the Label Priority Ranking window, I moved "MajorRoads - Shield" above "MajorRoads - Name" and positioned both above "Road." 

Finally, I added the essential elements to the Layout tab, carefully checking that each label was correctly placed and the visual hierarchy made sense. I exported the completed project, transforming it from a cluttered, confusing map into a clean, visually engaging, and informative street map of New York.

Through this meticulous process, I learned to leverage advanced GIS tools and techniques to create a map that communicates essential information clearly and effectively. What began as a jumbled mess became a well-organized and attractive map, telling a story of the city’s streets and boundaries with precision and style.

## Lessons Learned:

This project taught me several valuable lessons in map organization, label management, and the use of advanced GIS tools. I began by transforming a cluttered street map of New York into an organized and visually appealing representation. Labeling the borderline along the Hudson River between New York and New Jersey required creating distinct labels for each state, which I accomplished by carefully setting up label classes and configuring their appearance and placement. 

Through the process, I learned the importance of using SQL query expressions to label subsets of features, such as differentiating road names and shield numbers within the MajorRoads feature class. This exercise highlighted the power of data-driven symbology and precise label management to enhance map readability. 

I also discovered the significance of label weights and priorities in resolving potential conflicts and ensuring that the most important information is clearly displayed. By fine-tuning these settings, I could control the placement of overlapping labels effectively. 

Overall, this project deepened my understanding of the principles of visual hierarchy and effective map design. It demonstrated how thoughtful organization and the strategic use of GIS tools can turn a chaotic dataset into a clear and informative map, showcasing my ability to create compelling and accurate visual representations.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Map of Massachusetts:** [Map of Massachusetts](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Map-of-Massachusetts)

**Athens Heat Risk Index:** [Athens Heat Risk Index](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-GIS-for-Climate-Action/Athens-Heat-Risk-Index)

**Population Map:** [Population Interactive Map](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Population-Interactive-Map)

## Repositories
**Profile:** https://github.com/T3ch12et

**Cartography Repository:** [ESRI MOOC Cartography](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography)

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio
