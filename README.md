#Website Optimization Readme
###How to Run Application
1. Visit the GitHub page [here](http://www.leogenerali.com/frontend-nanodegree-mobile-portfolio/ "Optimized Portfolio").
2. Enjoy the optimized pages!

###PageSpeed Score Changes
- Optimized the pizzeria image
- Minified and inline the CSS
- Font files only load the necessary fonts

###Getting Rid of Jank Changes
####Background Pizzas
- Changed the number of background pizzas generated on page load. The website used to create 200 pizzas. Now, the site creates a number of pizzas based on the width and height of the users browser window. For my desktop, this was typically around ~25. This GREATLY increased framerate.a
- Move var items = document.getElementsByClassName('mover') outside of updatePositions. It did not need to be recreated everytime updatePositions was run.
- Move other various variable declarations outside of for-loops

####Slider Pizzas
- Used more efficient DOM queries
- Moved dimension and width calculations outside of for-loop in changePizzaSize function.