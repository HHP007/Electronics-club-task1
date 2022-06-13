
# Smart Garbage Monitoring System Using Arduino 101

### Problem Statement
Make a smart Garbage monitoring system using IOT(arduino 101) to monitor the level of garbage in the bins.

### Ideation
The working Principle and mechanism of the project is as follows,

**Present technology & parameter:**

_Monitoring the level_

Ultrasonic sensor **sends data to** Microcontroller **Alert** to server

**Improvements:**
  
1) _Odour Alert_

Odour Sensor **sends data to** Microcontroller **Alert** to server

2) _Spill Alert_

RPi camera **detects** spills while throwing **Alert** real-time to the thrower

3) _Using a Garbage Leveller_

Trash Thrown **compressed** trash in bin **checking** Level

4) _Solar Powered_

Solar panel **powers**  the gadgets
	


|Process/Sensor|Notion|Advantages|Disadvantages|
|:----:|:----:|:----:|:----:|
|Level of garbage| Ultrasonic sensor is placed at the lid of the garbage bin and detect the amount of trash filled in it and send it real time to the server.|The work and time spent of the collector is reduced, as he could reach to the spot only if it is about to fill and ignore it if it's not filled|Since the garbagelevel can't be plain always, the level deteccted by the sensor is not exact, so a leveller is required|
|Odour Alerter|Alert to the collector if there is any hazardous gas detected or something untolerable using an odour alert sensor.|Avoid the smell of bins on the residential area.|No cons.|
|Spill alerter|Alert to the user to throw it in the bin properly if there is a spill using a RPi camera module to detect it.|Keep the surroundings of the bin be kept clean.|Increase in the sensor cost and also the complexity of the code written to detect the spillage.|
|Leveller|Use a leveller(may be a steel plate) to press on the garbage to compress it to its minimum level.which can then be loaded with more trash and the sensor can detect the level more precisely.|If the added garbage is compressed then more thrash can be put into it and the over-spilling can be reduced.|Hardware cost, Should use Pneumatics a bit costlier.|
|Solar Powering|Use solar panels to power the electronics sub-systems in it.| Reduces the cost of power management and also makes the device more eco-friendly|Solar panel costs a bit.|
|MQ-135 Sensor|The MQ-135 Gas sensors are used in air quality control equipment and are suitable for detecting hazardous gases. The MQ-135 sensor module comes with a Digital Pin which makes this sensor to operate even without a microcontroller. If you need to measure the gases in PPM the analog pin needs to be used. The analog pin is TTL driven and works on 5V and so can be used with most common microcontrollers.|An easy to use a sensor that gives us the quality of the air in terms of PPM. The sensor can be fitted inside the bin to find the PPM of the gases inside it.|Cool sensor!!|MQ-135 Sensor|The MQ-135 Gas sensors are used in air quality control equipment and are suitable for detecting hazardous gases. The MQ-135 sensor module comes with a Digital Pin which makes this sensor to operate even without a microcontroller. If you need to measure the gases in PPM the analog pin needs to be used. The analog pin is TTL driven and works on 5V and so can be used with most common microcontrollers.|An easy to use a sensor that gives us the quality of the air in terms of PPM. The sensor can be fitted inside the bin to find the PPM of the gases inside it.|No cons|


The notion of the project is to use the Ultrasonic sensor to detect the garbage level and level it before detecting. It uses odour sensors to detect any hazardous sensors and transmit it in real time to an app. Also it detects for any spillage while any user throws garbage in the bin and notifies them to throw it properly. 
