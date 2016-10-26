---
layout: default
title: 3-Blink
---

# 3.0 - Blink

Building on our `Blink` skillz, lets build a LED circuit and control it with UNO!

For this project you will need a breadboard, some jumper wires, a 330 ohm resistor, and an LED. 

![led](images/led1.JPG)

> Know your LED: the longer leg is the `anode` and connects to positive voltage, i.e. `+` or `5V`; the short leg is the `cathode` and connects to ground, i.e. `-` or `GND`.  

> Know your resistor: resistors are marked by color bands, but they are often hard to read - check them with a multimeter.

# 3.1 - First circuit

1. Gently push the legs of your LED into two different rows on the breadboard. Remember which one is the long leg! 

    ![led](images/led2.JPG)

2. Connect the LED `cathode` (short leg) to `GND` by inserting the legs of a 330 ohm resistor into the row and the `-` Rail. 

    ![led](images/led3.JPG)

3. Connect the LED `anode` (long leg) to `5V` by inserting a jumper wire into the row and the `+` Rail. 

    ![led](images/led4.JPG)

4. Connect the breadboard to the UNO's power supply: 
- use a red jumper wire to connect the `+` rail to the pin labeled `5V` on the UNO. 
- use a black jumper wire to connect the `-` rail to any pin labeled `GND` on the UNO (you have 3 choices). 

    ![led](images/led5.JPG) 

    ![led](images/led6.JPG)

5. Plug your UNO into your usb cable. 

You should now have a beautiful glowing LED!

# 3.2 - Blink it! 

This circuit is drawing power from UNO, but it is not controlled by it. We need to connect the LED to a pin so we can start blinking!

1. Unplug the wire connecting the `anode` from the `+` rail. 

2. Connect the `anode` wire to pin `10` on the UNO. 

    ![led](images/led7.JPG) 

    ![led](images/led8.JPG)

3. On the IDE `Blink` sketch, replace `LED_BUILTIN` with `10`. The basic code should look like:

        void setup() {
            pinMode(10, OUTPUT);
        }

        void loop() {
            digitalWrite(10, HIGH);
            delay(1000);
            digitalWrite(10, LOW);
            delay(1000);
        }

4. Plug UNO into the usb, and click the upload arrow to load the sketch.

You should now have a beautiful **Blinking** LED! 

# 3.3 - Extra credit

- make an interesting pattern blinking both the LED and LED_BUILTIN.
- add another LED and make them blink together.
