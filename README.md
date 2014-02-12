flot-orderBars
==============

Fork of the Flot OrderBars plugin found here: http://www.benjaminbuffet.com/public/js/jquery.flot.orderBars.js

Improvements
============

### Compatability with IE8
IE8 doesn't support [Array.indexOf()](http://www.w3schools.com/jsref/jsref_indexof_array.asp). So I changed emmerichs Array.indexOf to [jQuery.inArray()](https://api.jquery.com/jQuery.inArray/).

### Compatability with Flot Stack Plugin (made by emmerich)
The main improvement I've made is compatability with the [Flot Stack plugin](https://github.com/flot/flot/blob/master/jquery.flot.stack.js).

To use the 2 together:
* Ensure that your data is well formed. Each series should contain a bars object with an order integer, like so:
```javascript
  var series = [];
  
  series.push({
      data: [], // your raw data
      bars: {
          order: 0
      }
  });
  
  series.push({
      data: [], // your raw data
      bars: {
          order: 1
      }
  });
```

* Ensure that the order bars plugin is loaded __before__ the stack plugin.

See the example for more information.


