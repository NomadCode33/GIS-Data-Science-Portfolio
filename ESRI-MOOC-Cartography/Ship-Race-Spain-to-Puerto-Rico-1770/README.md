# Ship Race: Spain to Puerto Rico (1770)
A stop-motion animation depicts two ships, El Rey and El Colon, racing across three different routes to determine which journey is the fastest.

<img src="./ShipRace Spain to Puerto Rico, 1770 720p.gif" img alt = "ShipRace GIF"/>

## How It's Made:

**Tech used:** ArcGIS Pro

The file opens with the interpolated ship paths active, showing each frame of the ship moving along its path. To animate the ships properly, several steps were necessary. First, I defined a per-feature filter using a range. A range filter connects to any numeric field and interactively filters features in the map. This filter was connected to the Hours_Travelled field, indicating how long it has been since the ship left port. By stepping through individual feature locations and synchronizing them with the exported video frames, the illusion of a ship moving across the ocean was created.

In the Bookmarks, I navigated to the Race Across Atlantic section and selected the Starting Line Bookmark. On the Logged Positions layer in the Contents pane, I accessed Properties to add a range filter. For the Start Field, I chose HOURS_TRAVELLED. I repeated this process for the Interpolated Positions layer. After completing the setup, a slider appeared on the right side of the view and a Range tab appeared on the ribbon. To activate the filter, I clicked the Range Disabled button. In the Range tab, under the Current Range group, I set the Max to 24 and Span to 0. Since the span was 0, the minimum value updated to 24 to match the maximum value. This minimum value represented 24 hours into the journey, or one day at sea. The span value of 0 meant one slice of data; a span of 10, for example, would show 10 hours of content and multiple ships. In the Step group, I clicked the Use Range Span button and set the Step Interval to 2.

Next, I used the range filter to create a stop-motion animation. I needed to create one image, or frame, in the final video for each defined position of the ships. I zoomed to the Starting Line bookmark, ensured the range slider was reset to the beginning of the range, opened the Animation Timeline pane, and created the first keyframe for the animation. Before adding the rest of the keyframes, I set the append time to create an animation that shows 25 individual states of the range slider per second. I then imported the remaining keyframes from the range slider steps. This process created an animation with 422 keyframes, one for each two-hour step, resulting in a total playing time of about 16.8 seconds. The final animation output was intended for YouTube format.

To update the last keyframe to show the end of the race, I selected the 422nd keyframe to set up the camera as needed. The last keyframe represents the slowest ship's arrival. I needed the camera to reach the finish line when the fastest ship arrived and hold that view until all ships finished. The data indicated that the winner arrived after 29 days of travel, which meant 348 (29 x 12) range slider steps. Therefore, the arrival keyframe was #349. I zoomed to keyframe 349, then to the Finish Line bookmark, and clicked Update on the Animation tab in the Edit group. To verify the camera path, I zoomed to the Racetrack bookmark, which initially showed a straight line not keeping the ships in view. To ensure the camera followed the ships, I updated the immediate keyframes. In the Animation pane, I scrolled to keyframe 70, selected it, and updated it in the Edit group of the Animation tab. I repeated these steps for keyframes 150 and 250, verifying the camera track on the Racetrack bookmark. Now the camera followed the ships, flying ahead as they crossed the Atlantic.

With the camera controls properly set, it was time to add lead-in and lead-out sections. The video began abruptly, potentially causing viewers to miss important information. In the Animation tab of the Playback group, I clicked the reset button to restart the animation from the beginning. In the Animation Properties pane, I set the Append Time to 3 seconds and checked the Append Front box to provide context for the race's starting point. I zoomed to the Overview bookmark and clicked Append in the Create group of the Animation tab. To finish, I went to keyframe 423 in the Animation Timeline pane, unchecked the Append Front box, and added a three-second lead-out section to show the full extent of the race upon completion. In the Create group of the Animation tab, I clicked Append.

With the video looking great, I needed to add title text and an overlay image to convey information to the audience. At keyframe 424, I pressed Ctrl + A to select all keyframes. In the Animation tab's Overlay group, I expanded the gallery and clicked Paragraph. I added the title, adjusted the font settings for clarity, and positioned it at the top center. To add an image overlay, I clicked Image in the same Overlay group, set the scale to 40% in the Appearance section, and positioned it at the top left. Finally, I set the appropriate video options and exported the video.

## Lessons Learned:

Throughout this project, I learned the importance of meticulous planning and attention to detail. Defining per-feature filters and synchronizing them with exported video frames taught me the value of precision in creating realistic animations. Handling a large volume of keyframes and ensuring smooth camera transitions highlighted the significance of methodical organization and iterative verification. Adding lead-in and lead-out sections, title text, and overlays emphasized the need to consider viewer engagement and comprehension. Overall, this project reinforced the importance of combining technical skills with effective organization to achieve successful results.

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
