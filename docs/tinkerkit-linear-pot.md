<!--remove-start-->
# TinkerKit - Linear Potentiometer

Run with:
```bash
node eg/tinkerkit-linear-pot.js
```
<!--remove-end-->

```javascript
var five = require("johnny-five");

new five.Board().on("ready", function() {
  new five.Sensor("I0").scale(0, 255).on("data", function() {
    console.log(Math.round(this.value));
  });
});


```


## Breadboard/Illustration


![docs/breadboard/tinkerkit-linear-pot.png](breadboard/tinkerkit-linear-pot.png)

- [TinkerKit Linear Potentiometer](http://www.tinkerkit.com/linear-pot/)
- [TinkerKit Led](http://www.tinkerkit.com/led/)
- [TinkerKit Shield](http://www.tinkerkit.com/shield/)


<!--remove-start-->
## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
<!--remove-end-->
