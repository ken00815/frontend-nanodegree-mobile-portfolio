##Running instructions
1. Open index.html in your browser (Google Chrome is highly recommended).
2. Click the hyperlinks if you want to see further.
3. For the pizzeria, you can use the slider to change the size of the pizza images.

## Optimizations details for index.html
1. Split the css code for printing into other css file and add "print" media query for it. So that those CSS code will not be rendering while users are not printing.
2. Inline the CSS code for moblie screen size and add media query 
..1. Minimize one time render blocking with mobile screen
..2. Those CSS code will not be rendered with larger screen. 
3. Inline the rest of CSS code, because those properties are only used for once. Therefore the render blocking can be minimized.
4. both scripts added "async", the webpage can be rendered and will not wait for the JavaScript.
5. Minimize the images resolutions and size since the photos are displayed in a small grids. It is not necessary to have such high quality and sizes.

## Optimizations detials for views/js/main.js for pizza.html
1. Directly assign the width of different sizes of the slider reflects. Therefore determineDx() is necessary, otherwise this function will be keep running.
2. In function updatePositions(), the position of the pizzas will re-calculate everytime with the large for-loop. Actually the results of the for-loop repeats. Therefore, it is unnecessary to run the for-loop with 200 times. 