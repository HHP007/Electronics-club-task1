

# Auto Intensity Control of Street Lights

### Problem Statement : 
Controlling the intensity of the street light based on the time and the lighting of the environment.

**Ideation and Planning : Mechanism**   

DS1307 Real time clock -- LDR -- Microcontroller -- LCD Display of Time -- Street light Intensity
### Part of the Pipeline to break : 

|Process/sensor	| Notion	| Advantages | Disadvantages |
|---------------------|-------------|------------|---------------|
|Real time clock (DS-1307)|	To keep record of the time  as the intensity of the light is to be varied based on it	|Accurately keeps track of seconds, minutes, hours, ability to generate Programmable Square wave. Low current use.|	Loses about 5 seconds a day as compared to NIST's time of day.|
|LDR	|To change the intensity of the light depending on the light around the surrounding environment|	Using LDR and RTC produces accurate results. High sensitivity, easy employment, Low cost, High light-dark resistance ratio.|	Low temperature stability for the fastest materials, slow response in stable materials.|
|ATmega8	|Low power CMOS 8-bit microcontroller based on the AVR RISC architecture, executes powerful instructions in a single clock cycle|	Generally contain 3 timers/counters. While two 8-bit timers can also be used as counters, the third one is a 16-bit counter. These are used to generate precision output signals, count external events or measure parameters of input digital signal.|	Long procedures to write simple code  |
|LED Array|	Using High Intensity LED's saves energy, most commonly found street lights are High Intensity Discharge Lamps which consume a lot of power|	Using LED Array reduces the cost. Have longer lifetime. Low maintenance and power consumption, High efficiency.|	LED performance largely depends on the ambient temperature of the operating environment or thermal management properties.|

### Improvisation
We'll opt RTC .   
* The DS-1307 is often the default choice for an RTC.  
* The RV-1805 draws so little power that this Sparkfun module gets by without a backup battery at all.
* The DS3234 has the distinction of using an SPI interface instead of I2C.  
* The RTC Pi, a cheap and simple solution to keeping the Pi in sync when away from the Internet.  

### Prototyping phase : 
we connect the circuit and check if we get the expected results. Test and debugg it untill we receive get the expected results.
On persistance of the problem, reach out to the Ideation Phase and redo the parts which breaks apart in the actual circuit.  

**Limitations  :**   
* Even though energy is saved ,if there are any vehicles after fixed time, intensity of the light is low.  
* Maximum energy cannot be saved.  

