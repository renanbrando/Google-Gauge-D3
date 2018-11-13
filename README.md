# Google-Gauge-D3
This is a gauge styled graphic based in Tomer Doron’s with a few modifications and improvements. 

# Config Example
```
let config = {
  size: 200, // size of gauge
  label: label, // label to displayed
  min: min, // minimum value to be displayed
  max: max, // maximum value to be displayed
  minorTicks: 5, // interval between values
  // zones to filled with colors, intervals must contain from and to
  greenZones:[
      {
          from: 0, 
          to: 30
      }
  ],
  yellowZones:[
      {
          from: 30,
          to: 90
      }
  ],
  redZones:[
      {
          from: 90,
          to: 100
      }
  ]
}				
```

# Usage
```
var gauge = new Gauge( "GaugeContainer", config); // where GaugeContainer is the id of the div in html
gauge.render();
gauge.redraw(50, 5000, "%"); // 50 is the gauge displayed value, 5000 is the transition time and "%" is the unit to be displayed with the label (optional)
```
