# Auto Intensity Control of Street lights(debugging)

### Flow: DS-1307 Real time clock --> LDR --> Microcontroller --> LCD Display of Time --> LED Array

These are the major components which should be tested and debugged incase of issues.
Check if all the modules light up.

**No?** Then the module which does not glow might have been mishandled and shorted or the connections might be wrong or loosely connected. 
* If shorted we have to replace it with another one, 
* If misconnected go through the data sheet and connect it properly and intact.

**Yes?** Then go with the below ones on testing everything individually

Check if some module is **hot?**

Then there is a problem with the circuit .We might notice it behave differently in sometime as something might burn.So replace it and check the connections properly that might be responsible for burning the module.

**Testing RTC :** 

We could connect Master I2C/SMBus Engine tool(if we used it) and the DS-1307 together (with pull-ups and other essentials of course) and check if you can communicate with the DS-1307 in a few minutes. If you can, then DS1307 is working and it could be your C code which could potentially cause an error.
	
**Testing LDR :** 

Digital multimeter is used to test LDR(Light dependent resistance). We all know that the resistance of an LDR varies according to the light falling on it. At bright light, the LDR resistance will be around 500Ohms and at darkness the resistance will be around 200K. For a proper diagnosis we need to measure the resistance of the LDR at bright light and at darkness. 
1) In bright light connect the LDR leads to multimeter terminals the resistance is expected to be low around 500 ohms, 
2) Next cover it with an opaque paper and measure the resistance is expected to be high around 200 K ohms. 

If the resistance values under different conditions show the same trend then LDR is working properly.
	
**Testing ATmega8 :** 

If we notice
* RTC lights up
* LDR lights up
* couldn't upload code to ATmega8 or
* IC is hot
We would have probably burnt it , but shorting an ATmega8 isn't easy , they have inbuilt mechanisms to prevent it so check other components before concluding that the ATmega8 might have shorted.

**Testing LCD Display :** 

* Add your LCD display and potentiometer to your breadboard. 
* Connect the power and ground pins on your LCD, which are Pins 15 and 16, respectively. 
* Connect the ground and power for your LCD’s backlight, which are Pins 1 and 2, respectively. 
* Connect the control pins for your LCD to the digital pins on your Arduino. 
* Now connect the potentiometer, which controls the display’s contrast. The center pin of the potentiometer should go to Pin 14 of the LCD display and the other two pins of the potentiometer are connected to power and ground, in any order. 

Upload some code to make sure that the LCD is working properly. This code is the first part of your alarm clock sketch. You build upon it to add all the other functions for your clock. When this code is uploaded, you should see the message displayed on the LCD. 

If you don’t see anything, or if the display has garbled characters, you’ve connected something incorrectly. Go back to the wiring table.

**Testing LED's :** 

Multimeter is used to test the LEDs. The multimeter with a diode setting is needed and the red and black test leads should be connected to the outlets on the front of the multimeter. 
The red lead is the positive charge. The black lead is the negative and should be plugged into the input labelled COM. Connect the black probe to the cathode and the red probe to the anode, this connection should cause the LED to light up. 

When the probes are touching the cathode and anode, an undamaged Led light should display a voltage of approximately 1600 mV. If no reading appears on your screen during the test, start again to make sure the connections were made properly. If you have performed the test properly, this may be a sign that the LED light is not working. Replace the LED with a new one. 
	
Using the above mentioned methods we can test and Debug all the components of the circuit one by one based on the suspicions we identify and following this method recursively we can get the circuit working.
	

## Resources

Here are some resources used in this projects

[ATmegs8 features](https://docs.rs-online.com/5d80/0900766b815965d2.pdf)

[DS-1307 datasheet](https://www.sparkfun.com/datasheets/Components/DS1307.pdf)

[RTC features](https://www.elprocus.com/rtc-ds1307/)

