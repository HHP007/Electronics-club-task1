
# Auto Intensity control of Street lights  

## Description
We Control the Intensity of street light using Pulse width modulation.The PWM is adjusted by microcontroller to increase or decrease the intensity of street lights based on the peak hours. 
The peak hours can be calculated by considering parameters like traffic density, time, light intensity of the environment. 
LDR is used to find the light intensity of the environment. It is connected to ADC pin of the microcontroller since LDR is analog in nature. 
RTC( Real time Clock) is used to find the current time , LCD display is used for displaying the time read using RTC, LED array is the number of high power LED's connected in series.

It is connected to PWM pin of the micro controller. The LDR is placed in darkness as the street lights switches on only when there is no light on LDR. Now if the time is between 9 PM and 3.30 AM, 
then street light glows with full intensity, from 3.30 PM intensity of the light slowly starts decreasing and finally in early morning when the light intensity increases the LDR detects it and the street light glows with very less intensity. 
By 6AM, the light completely goes off.

Circuit Components

    ATmega8 micro controller
    DS1307 IC
    Light Dependent Resistor
    LED array.
    LCD display

## Circuit Diagram
![](https://www.electronicshub.org/wp-content/uploads/2014/06/Auto-Intensity-Control-of-Street-Lights-Circuit-Diagram-768x367.jpg)

The web link for the detailed description of the project: [Auto Intensity control of Street lights ](https://www.electronicshub.org/auto-intensity-control-of-street-lights/)