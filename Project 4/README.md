Project 4
===============================

Welcome to the pizzeria. Double click index.html to open the site. I have made numerous optimizations to get pagespeed insight score of 92. Also, made improvements to eliminate forced synchronous layout. Note, I have included an unminified version of index.html called index-clean.html. Use that if you would like to read it.

Optimizations made for pagespeed insight
1. used async for google analytics javascript
2. Minified html
3. Moved all css inline so a call to separate css file was not needed
4. Compressed images. I used the following:
	Use this site first: http://www.jpeg-optimizer.com/
	Use this program next: https://imageoptim.com/


Eliminate forced synchronous layout
1. Used Chrome timeline to find issues: http://i.imgur.com/bzF9G7i.png
2. Modified changePizzaSizes function to no longer have to change from percentage
3. created randomPizzaContainer variable to not repeat and follow dry convention
      var randomPizzaContainer = document.querySelectorAll(".randomPizzaContainer");
    for (var i = 0; i < randomPizzaContainer.length; i++) {
      // var dx = determineDx(randomPizzaContainer[i], size);
      // var newwidth = (randomPizzaContainer[i].offsetWidth + dx) + 'px';
      randomPizzaContainer[i].style.width = newwidth + "%";
    }
4. Removed determineDx and sizeSwitcher functions
5. Simplified conversion from percentage to instead whole number. e.g.
6. Created a separate for loop to improve performance since there are only five possible results
7. storing in variable, so it does not have to be checked each time in loop

