chartjs-custom
======

The fork version of [nChart]

## Usage

```js
var Canvas = require('canvas')
  , canvas = new Canvas(800, 800)
  , ctx = canvas.getContext('2d')
  , Chart = require('nchart-custom')
  , fs = require('fs');
 
new Chart(ctx).Doughnut(
    [
        {
            "value": 50,
            "color": "#27ae60",
          "showCenterText":true,
          "showCenterLabel":true,
          "label":"Compliance"
        },
        {
            "value": 100,
            "color": "#D4CCC5",
            "label":"Non-compliance",
            "color": "#F7464A"
        }
    ]
  , {
        scaleShowValues: true,
        percentageInnerCutout : 75,
         scaleFontSize: 24
    }
);
 
canvas.toBuffer(function (err, buf) {
  if (err) throw err;
  fs.writeFile(__dirname + '/pie2.png', buf);
});

```
## Installation

    $ npm install -g nchart

## Required!

  * [node-canvas][]

## Documentation

  You can find documentation at [Chart.js Doc][]

## Thanks to

  * https://github.com/visionmedia
  * https://github.com/nnnick

## License

  [MIT](LICENSE)

[node-canvas]: https://github.com/Automattic/node-canvas
[Chart.js Doc]: www.chartjs.org/docs/
