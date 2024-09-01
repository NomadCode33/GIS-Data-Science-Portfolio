# Ship Race: Spain to Puerto Rico (1770)
A stop-motion animation depicts two ships, El Rey and El Colon, racing across three different routes to determine which journey is the fastest.

<img src="./ShipRace Spain to Puerto Rico, 1770 720p.gif" img alt = "ShipRace GIF"/>

## How It's Made:

**Tech used:** ArcGIS Pro

The project opened with an animated display of interpolated ship paths, showing each ship’s movement frame by frame. To bring the animation to life, I needed to take several steps. First, I set up a per-feature filter using a range. This filter, connected to the "Hours_Travelled" field, allowed me to interactively filter the features on the map based on how long each ship had been at sea since leaving port. By synchronizing these filtered features with the exported video frames, I created the illusion of ships sailing across the ocean.

I navigated to the "Race Across the Atlantic" section in the bookmarks and selected the "Starting Line" bookmark. From there, I went to the "Logged Positions" layer in the Contents pane and opened the properties to add a range filter. I set the start field to "HOURS_TRAVELLED" and repeated this process for the "Interpolated Positions" layer. With the setup complete, a slider appeared on the side of the view and a "Range" tab on the ribbon. I activated the filter and set the maximum value to 24 and the span to 0, effectively showing a 24-hour snapshot of the journey. This allowed the animation to display each frame as a single day at sea, creating a stop-motion effect. 

Next, I used this range filter to build a stop-motion animation. I created individual images (frames) for each defined position of the ships. I zoomed to the "Starting Line" bookmark, reset the range slider, opened the Animation Timeline pane, and created the first keyframe. Then, I set the append time to display 25 states of the range slider per second and imported the remaining keyframes. This process generated an animation with 422 keyframes, one for each two-hour step, resulting in a total playtime of about 16.8 seconds, formatted for YouTube.

To mark the end of the race, I adjusted the final keyframes. I selected the 422nd keyframe and set up the camera to show the finish line. The fastest ship arrived after 29 days, meaning the keyframe for this moment was #349. I zoomed to keyframe 349, navigated to the "Finish Line" bookmark, and updated the camera. I verified the camera path, ensuring it tracked the ships smoothly by adjusting keyframes at intervals. Now, the camera followed the ships closely as they raced across the Atlantic.

With the animation set, I added lead-in and lead-out sections to provide context. To avoid a jarring start, I reset the animation to the beginning and added a three-second introduction. I zoomed to the "Overview" bookmark and clicked "Append" to create a smooth opening. To close, I added a three-second lead-out to highlight the race's conclusion.

Finally, I added title text and an overlay image to enhance viewer understanding. At keyframe 424, I selected all keyframes and added a title using the overlay tools. I adjusted the font for clarity and positioned it at the top center of the screen. I then included an image overlay, scaled to 40%, at the top left for additional context. After setting the final video options, I exported the completed animation.

This project transformed static data into a dynamic, engaging visual narrative, capturing the excitement of a race across the Atlantic and effectively communicating the story to the audience.

## Lessons Learned:

Throughout this project, I learned the importance of meticulous planning and attention to detail. Defining per-feature filters and synchronizing them with exported video frames taught me the value of precision in creating realistic animations. Handling a large volume of keyframes and ensuring smooth camera transitions highlighted the significance of methodical organization and iterative verification. Adding lead-in and lead-out sections, title text, and overlays emphasized the need to consider viewer engagement and comprehension. Overall, this project reinforced the importance of combining technical skills with effective organization to achieve successful results.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Shipping in 1770:** [World Shipping in 1770](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography/Shipping-in-1770)

**Lynnwood Right-of-Way:** [Lynnwood Right-of-Way](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Furtado-and-Associates-Projects/Lynnwood%20Right-of-Way)

**Climate Change Report:** [Climate Change Report](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/Climate-Change/project-report-saejinm)

## Repositories
**Profile:** https://github.com/T3ch12et

**Cartography Repository:** [ESRI MOOC Cartography](https://github.com/T3ch12et/GIS-Data-Science-Portfolio/tree/main/ESRI-MOOC-Cartography)

**Main Repository:** https://github.com/T3ch12et/GIS-Data-Science-Portfolio
