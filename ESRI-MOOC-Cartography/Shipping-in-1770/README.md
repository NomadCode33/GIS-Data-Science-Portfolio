# World Shipping in 1770
This animation provides a 2D visualization of the shipping routes of England, the Netherlands, and Spain in the year 1770, dynamically unfolding through time.

<img src="./ShippingIn1770_gif_640x720p(3).gif" img alt = "Shipping in 1770 GIF"/>

## How It's Made:

**Tech used:** ArcGIS Pro

After downloading the data, I opened the map and navigated to the Properties of the Ship Positions layer. In the Time tab, I selected "Filter Layer Content Based on Attribute Values" and confirmed that each feature has a single time field, setting the Time Field to ShipDate. With these settings confirmed, the time slider appeared, displaying a timeline from January 1, 1770, to December 31, 1770. In the Snapping group, I checked the Time Snapping box and set the units to Days, with a span of 7 days, making the time slider jump ahead by one week intervals.

I then enabled the Colonial Ports and Ship Paths layers in the Contents pane. The map's brightness was overwhelming, making it difficult to see all the details. To improve visibility, I adjusted the transparency in the Effects group: 50% for the Colonial Ports layer and 90% for the Ship Paths layer. This adjustment made the Ship Positions more prominent, while the paths and ports receded. Next, I changed the background color to a custom dark gray in the Map Properties, creating a more cohesive and less stimulating visual.

The next step was to create temporal keyframes to illustrate changes in ship positions over the year. I first defined the change in temporal extent for each time step, establishing the first keyframe in the animation. In the Time tab, within the Current Time group, I verified that the Span was set to 7 days, locked it, and confirmed that the Start field was set to January 1, 1770. I then moved to the View tab, clicked the Add Animation button in the Animation group, and opened the Animation Timeline pane. I created the first keyframe and, in the Export group, selected Movie to open the Export Movie pane. Although I initially chose the Twitter preset, I switched to the YouTube preset for a wider resolution. I panned the map to place Antarctica at the base of the frame, leaving some blank space at the top for the title. I selected the first keyframe on the Animation Timeline, clicked Update, and set the spatial extent.

Back in the Time tab, I confirmed the Span was still 7 days and locked, with the End field now set to December 31, 1770. Returning to the Animation Timeline pane, I clicked the Append Next Keyframe button to add a second keyframe. To ensure the duration was easy to follow, I set it to 12 seconds in the Playback group of the Animation tab.

To communicate the changing dates effectively, I included dynamic dates within the video. I selected both keyframes in the Animation Timeline pane, updated the title in the Overlay Group to "World Shipping (1770)," and set the font. In the Dynamic Text section of the Overlay group, I selected Map Time, adding the predefined tagged HTML element `<dyntype="animation" property="endTime" format="short"/>` and matched the font to my earlier setting. The end date for the first keyframe (January 8, 1770) appeared in the upper-left corner, dynamically updating in sync with the video.

I modified the `<dyn 'endTime">` element to `<dyntype="animation" property="endTime" format="MMMM"/>` to display only the month name. I positioned it at the bottom-center and, in the Animation Properties pane, clicked the gear icon next to the endTime overlay item to access advanced text properties. I chose None from the Callout drop-down list, simplifying the presentation and making the dynamic text easier to read during fast playback. Finally, I exported the animation using the appropriate video settings, completing the process.

## Optimizations

The resolution could be slightly shorter, as the empty space risks breaking immersion. However, it could also be seen as part of the setpiece, ultimately making it inoffensive in the long run.

## Lessons Learned:

I relish the feeling of being a director creating my own movie. Through this process, I've gained a deeper understanding of how to make animation meaningful and informative for the viewer. It requires a great deal of foresight and planning to ensure that each frame is meticulously crafted, much like directing a flawless movie scene. Without these fundamental skills, an animation can easily become all style and no substance.

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
