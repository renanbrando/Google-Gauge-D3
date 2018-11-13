# Google-Gauge-D3
This is a graphic gauge styled based in [Tomer Doron’s](http://bl.ocks.org/tomerd/1499279) with a few modifications and improvements. It is also an implementation of [Google's gauge chart](https://developers.google.com/chart/interactive/docs/gallery/gauge).

# Usage
![alt Gauge Chart](https://i1.wp.com/blog.novatrend.ch/wp-content/uploads/2018/01/01-gauge.gif?fit=747%2C271&ssl=1)

To use this gauge you must have gauge.js and d3 library imported to your application. An example can be found in index.html.

# Config Example
```
let config = {
  size: 200, // size of gauge
  label: label, // label to displayed
  min: min, // minimum value to be displayed
  max: max, // maximum value to be displayed
  minorTicks: 5, // interval between values
  // zones to filled with colors, intervals must contain from and to
  greenZones: {
    from: 0,
    to: 50
  },
  yellowZones: {
    from: 50,
    to: 90
  },
  redZones: {
    from: 90,
    to: 100
  }
}				
```

# Usage Example
```
var gauge = new Gauge( "GaugeContainer", config); // where GaugeContainer is the id of the div in html
gauge.render();
gauge.redraw(50, 5000, "%"); // 50 is the gauge displayed value, 5000 is the transition time and "%" is the unit to be displayed with the label (optional)
```
