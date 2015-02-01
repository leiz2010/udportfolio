## Website Performance Optimization portfolio project

Lei zhang  
1/13/2015  

First objective of this project is to optimize Cameron's profilo to
score 90 or better for the index.html on both mobile device and desktop
computer at https://developers.google.com/speed/pagespeed/insights/  
Second objective is to display at 60fps when scrolling in pizza.html.  
Third objective is to achieve 5 ms when pizzas resize in pizza.html.  

Github link to the project: https://github.com/leiz2010/udportfolio  

Github host link URL: http://leiz2010.github.io/udportfolio/  

Clone the repo to your local computer to see the fixes with the Github
project link above or open the host link URL in web browser to see the
live project.  

Fixes added:  

Index.html fixes:
  1. Changed to inline CSS styles.
  2. Moved style links below script links.
  3. Added asynce for google-analytics.
  4. Load google font asynchronously.
  5. Added viewport.
  6. Added meida print.
  7. Compressed and resized profilepic.jpg and pizzeria.jpg

pizza.html fixes:  
  1. Changed to inline CSS styles.
  2. Removed unused CSS styles in twitter bootstrap.
  3. Added viewport.
  4. Compressed pizza.png.

main.js fixes:  
  1. Refactored changePizzaSizes function.
  2. Refactored updatePositions funtion.
  3. Added requestAnimationFrame for updatePosition and changePizzaSizes.
  4. Added tick and OnScoll function to control rAF.
  5. Used CSS transform with translateX.
  6. Added 	-webkit-backface-visibility: hidden;
     -webkit-perspective: 1000; in .mover it handle flicker from
     GPU acceleration. (Not entirely sure if translateX triggers
     the GPU acceleration, but pizza images seems to in a separate
     layer now).
  7. Refactored the anonymous function at bottom of main.js.  

Reference:  
http://davidwalsh.name/translate3d  
http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/  
http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/  
https://www.igvita.com/2014/05/20/script-injected-async-scripts-considered-harmful/#comment-1398899164  
https://piazza.com/  

Special thanks to Kevin Mayo and Haopei Yang for answering my question on
reducing painting time in https://piazza.com/
