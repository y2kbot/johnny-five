<!--remove-start-->
# TinkerKit - Gyro

Run with:
```bash
node eg/tinkerkit-gyroscope.js
```
<!--remove-end-->

```javascript
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  // Create a new `Gyro` hardware instance.

  var gyro = new five.Gyro({
    pins: ["I0", "I1"],
    sensitivity: 0.67
  });

  gyro.on("change", function() {
    console.log("X raw: %d rate: %d", this.x, this.rate.x);
    console.log("Y raw: %d rate: %d", this.y, this.rate.y);
  });
});

```








<!--remove-start-->
## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
<!--remove-end-->
