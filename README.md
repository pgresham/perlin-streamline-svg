# A Perlin Streamline UI and SVG Generator 

## What it is:

This program is an implementation of the Streamlines repository by Andrei Kashka (https://github.com/anvaka/streamlines), adding a HTML-based UI which allows for partial manipulation of the output as well as a way to download the linework as an SVG file.

It was developed with the pen plotter in mind, and generates detailed, albeit large vector files for this purpose. 

## How to get it and run it:

To download, you can use: `git clone https://github.com/pgresham/perlin-streamline-svg` to obtain all files  
...or download the zip and extract it into a folder.

Running the program is fairly straightforward: with both the HTML and JavaScript file in the same directory, opening the `index.html` file in a browser should start the program. This has been tested in both Chrome and Firefox browsers, but should work in others. 
__Please note:__ this program creates quite large files (5Mb to 50Mb+) depending on control states as noted below. This can also impact rendering time, especially on slower processors.

*It is recommended to run this through a local web server such as python's http.server module to ensure proper functioning.* 

## What the controls do:

Here is a basic breakdown of the controls:

+ __Generate SVG__ downloads an SVG file of the output in the preview screen. Color information is not downloaded;the vector file will be black line on a transparent background.
+ __Redraw__ reruns the vectors using the current slider settings.

+ __dSep__ defines the separation between the streamlines and therefore the number that are generated. Higher dSep, fewer lines.
+ __Freq__ changes the "loopiness" of the streamline vectors by increasign the wave frequency.
+ __k__ changes the scale of the Noise. a higher k value creates more "textured" streamlines.
+ __LERP__ or linear interpolation changes the smoothing of streamlines between parts of the generated matrices. Anything above 1 and the grid will begin to show through.

+ The __Algorithms__ (Benjamin, Flusser, McLuhan, and Manovich) change the ways in which the streamlines are rendered. They are noted at around lines 179 to 210 of the `bundle.js` file and can be changed as needed.

+ __Line Color__ and __Background Color__ change the colors of the preview window. As noted above, this color information is not included in the SVG output.

 <img width="100%" alt="An image of the streamlines UI running" src="https://github.com/user-attachments/assets/64a49563-98d3-480d-bfcd-48a6def3d115" />

---

*Attributions: as noted above, the heavy lifting of this code including the Streamlines algorithm is the work of Andrei Kashcha (C) 2018-2025, https://github.com/anvaka/streamlines and is used here under the MIT License. Additional code implemented within Kashcha's original work is (C) 2018 by Gerard Ferrandez (https://codepen.io/ge1doot/pen/GQobbq) also used under the MIT License. Additional implementations Bruno Jobard and Wilfrid Lefer's paper "Creating Evenly-Spaced Streamlines of Arbitrary Density" are also noted within the code https://web.cs.ucdavis.edu/~ma/SIGGRAPH02/course23/notes/papers/Jobard.pdf*  
