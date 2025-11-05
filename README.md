# Height-measurement-system

**Project by:** Hariom Sharma – *Srajnik Lab, Shiksha Sopan, IIT Kanpur*

---

##  Overview

This project is a **Height Measurement System** built using an **Ultrasonic Sensor** and an **Arduino**.
It measures the height of a person (or object) by comparing the detected distance from the sensor to a reference distance (recorded when no object is present).

The system displays both the **current distance** and **calculated height** on a 16x2 LCD display.
A push button allows the user to **reset or recalibrate** the reference (zero) level easily.

---

##  Components Required

* Arduino Uno / Nano
* HC-SR04 Ultrasonic Sensor
* 16x2 LCD Display (with or without I2C)
* Push Button
* Jumper Wires
* Breadboard / PCB
* USB Cable / Power Supply

---

##  Working Principle

1. The ultrasonic sensor emits sound waves and measures the time taken for the echo to return.
2. The Arduino converts this time into distance (in centimeters).
3. A **reference distance** is recorded when no object/person is under the sensor.
4. When a person stands below, the new distance is measured and **height = referenceDistance - currentDistance**.
5. The LCD continuously shows the measured **distance** and calculated **height**.
6. The **button** can be pressed anytime to reset the reference distance.

---

##  Circuit Connections

| Component    | Arduino Pin | Description                    |
| ------------ | ----------- | ------------------------------ |
| HC-SR04 Trig | D11         | Trigger signal                 |
| HC-SR04 Echo | D10         | Echo response                  |
| Push Button  | D8          | Reset reference (INPUT_PULLUP) |
| LCD RS       | D6          | Register Select                |
| LCD EN       | D7          | Enable                         |
| LCD D4       | D5          | Data pin 4                     |
| LCD D5       | D4          | Data pin 5                     |
| LCD D6       | D3          | Data pin 6                     |
| LCD D7       | D2          | Data pin 7                     |

---

##  Code Description

* **measureDistance()**: Sends a trigger pulse and measures the echo time to calculate the distance in cm.
* **setup()**: Initializes LCD and sets the reference height.
* **loop()**:

  * Continuously measures distance.
  * Calculates height difference.
  * Displays results on the LCD.
  * Allows resetting reference using the button.

---

##  Output Example

```
Dist: 45.3cm
Height: 155.0cm
```

---

##  Applications

* Smart height measuring device for schools or labs
* Automatic attendance or health monitoring setups
* Object level detection or non-contact distance sensing

---

##  Developed At

**Srajnik Lab – Shiksha Sopan, IIT Kanpur**
A community-driven innovation lab promoting hands-on learning in electronics and embedded systems.

---

