# pi-home-gpio

![Node.js CI](https://github.com/raspberry-pi-home/pi-home-gpio/workflows/Node.js%20CI/badge.svg)

## Usage

```
npm install --save https://github.com/raspberry-pi-home/pi-home-gpio.git
```

```
import { isAccessible } from 'pi-home-gpio'

console.log(isAccessible)
```

```
import { Led } from 'pi-home-gpio'

const led = new Led(17)

led.on()
setTimeout(() => led.off(), 1000)
```

```
import { PushButton, Led } from 'pi-home-gpio'

const led = new Led(17)
const button = new PushButton(4)

button.onAction(led.value)
```

```
import { ToggleButton, Led } from 'pi-home-gpio'

const led = new Led(17)
const button = new ToggleButton(4)

button.onAction(led.toggle)
```

## Documentation

### Led(pin)
Creates a new Led component which will act as a digital output

#### on()
Turns on the Led

#### off()
Turns off the Led

#### toggle()
Toggle the status of the Led

#### value([value (0|1)])
Set the given value to the Led, if *value* is not provided it will return the current status
If provided, *value* must be either `1` or `0`

---

### PushButton(pin)
Creates a new Button component which will act as a digital input

#### onAction(callback)
When the button is pressed `onAction` function is called

---

### ToggleButton(pin)
Creates a new Button component which will act as a digital input

#### onAction(callback)
When the button is pressed `onAction` function is called with a `1`, and when the button is released `onAction` function is called with a `0`

#### value()
Returns the current status (`1` or `0`)

---

### Concepts

#### - pin
##### pin numbers
* 2
* 3
* 4
* 5
* 7
* 6
* 8
* 9
* 10
* 11
* 12
* 13
* 14
* 15
* 16
* 17
* 18
* 19
* 20
* 21
* 22
* 23
* 24
* 25
* 26
* 27
