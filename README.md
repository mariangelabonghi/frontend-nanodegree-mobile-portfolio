# Website Performance Optimization portfolio project
##### The purpose of the project is to optimize this online portfolio for speed. In particular, changes have been applied to meet the following performance requirements:


### 1. Critical Rendering Path:
##### "index.html" achieves a PageSpeed score of at least 90 for Mobile and Desktop.
###### Actions made:
1. Inlined style CSS resource
2. Used js script for google fonts
3. Asynchronously load blocking resources
4. Compressed images; Optimized images; Resized images
5. Used media query for 'print' styles
6. Minified HTML; print.css and perfmatters.js

#### 1.1 Instruction:
- Clone the repository
- Expose the local server to the internet through ngrok [Read more here!](https://ngrok.com/)
- Insert the URL that makes tunnel with the localhost in the [PageSpeed Insight](https://developers.google.com/speed/pagespeed/insights/) and Analyze the speed

### 2.Frame Rate
##### Optimizations made to views/js/main.js make views/pizza.html render with a consistent frame-rate at 60fps when scrolling:
- Use of "requestAnimationFrame"
- The evaluation: "document.body.scrollTop / 1250", in the "updatePositions" function, has been moved out of the for loop
- Use of .transform and translate instead of .left in the for loop of the "updatePositions" function

#### 2.1 Instruction:
- Clone the repository
- Open "pizza.html" with the browser
- Analyze the frame rate during the page scrolling through the developer tool

### 3.Computational Efficiency
##### Time to resize pizzas is less than 5 ms using the pizza size slider on the views/pizza.html page. Resize time is shown in the browser developer tools.
- In the function "changePizzaSizes" all the evaluation of the list of the elements within the document, have been moved out of the loop
- In the function "changePizzaSizes",  there is the same DOM call twice. This call has been cashed into a variable.

#### 3.1 Instruction:
- Clone the repository
- Open "pizza.html" with the browser
- Open the developer tool
- Use the slider on the page to change pizza size and read the time to resize pizza in the console