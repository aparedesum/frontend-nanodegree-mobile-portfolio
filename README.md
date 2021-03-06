
####Part 1: How to run the project


1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)


####Steps for improving the performance:

1. I have inlined and minified the fonts (downloaded from http://fonts.googleapis.com/css?family=Open+Sans:400,700) and style.css in index.html.
2. I have added the asyn attribute in the scripts tag (index.html, project-2048.html, project-mobile.html,project-webperf.html).
3. I have merged the code inside script (index.html, project-2048.html, project-mobile.html, project-webperf.html) into perfmatters.js.
4. I have used http://www.willpeavy.com/minifier/ for reducing the html files (but not pizza.html).
5. I have used http://javascript-minifier.com/ and http://cssminifier.com/ for reducing all the js (but not main.js) and all the css files.
6. I have minified main.js into main.min.js and called from pizza.html.

####Changes in main.js
1. I calcule the number of pizzas (initially 200) in order to get a dynamic number of pizzas based on screen size.
2. I use pizzaArray for getting the references of the pizzas.
3. I use getElementBy instead of querySelector.
4. Refactor in for loops in order to reduce the calls to the DOM api wherever is possible.
5. Improved the updatePositions method (calculating the phases in a separate for loop and using the transform property).
6. I have minified main.js into main.min.js.
7. I have used http://optimizilla.com/ for optimizing the images.
