---
title: 'Traffic Light Sensor'
permalink: /traffic-light-sensor/
breadcrumb: 'Traffic Light Sensor'

---

**Contributed by Ms Chiam Lee Lee (Teacher), Aretha Lee and Pay Xinyi (Students) from Raffles Girls Primary School**

![1](/images/in-schools/digital-maker/projects/a-better-world/traffic-light-sensor/traffic-light-sensor1.jpg)

The project focuses on the safety of pedestrians near the traffic light junctions. When it is red man, the traffic light sensor will trigger the LED lights to blink, the warning message to display and the buzzer to sound when someone steps into the prohibited zone.

 

Once they move out of the zone, the LED lights will still be on and the warning message will still be displayed, but the buzzer will stop sounding. When the green man appears, the LED light and warning alert will be turned off.<br>

**You will need:**<br>

[Download Program Code](/files/projects/a-better-world/traffic-light-sensor-program-code.hex)<br>


1 x BBC micro:bit<br>
1 x micro USB cable<br>
2 x AAA batteries<br>
1 x Wooden cardboard<br>
2 x Spray paint<br>
1 x set Lego figurines and cars<br>
1 x Breadboard and Prototype Shield<br>
1 x Ultrasonic sensor<br>
1 x set LEDs for LED strip and red/green man<br>
1 x set Jumper wires<br>
1 x Buzzer<br>
2 x Synthetic glass patches<br>
1 x Wooden stick<br>

#### Instructions

![2](/images/in-schools/digital-maker/projects/a-better-world/traffic-light-sensor/traffic-light-sensor2.jpg)

**1.  Identify on an area of interest** <br>
Identify on an area of interest and brief study of data to confirm project.<br>

---

**2.  Brainstorm** <br>
Brainstorm for possible causes of the problem, using fishbone diagram.<br>

---

**3. Use mindmap** <br>
Use mindmap to guide and develop solutions to solve the problem.<br>

---

![3](/images/in-schools/digital-maker/projects/a-better-world/traffic-light-sensor/traffic-light-sensor3.jpg)

**4. Code the micro:bit**<br>
Initially, light sensor was considered, but after testing, it is concluded that the light sensor is not a good solution as the sensitivity of the light sensor depends on the lighting conditions on the road. For example, the light input to the input sensor will be different on cloudy day and night conditions.

Ultrasonic sensor is used to replace light senor. Ultrasonic sensor returns the distance of an object from the ultrasonic sensor and avoids sensing moving vehicle.

Components used<br>
• LEDs<br>
• Buzzer<br>
• Ultrasonic Sensor<br>
• Micro:Bit Display<br>
 
---

**5. Install LED strip**<br>
LED strip installed before restricted area to warn pedestrians not to cross beyond LED strip when it is Red Man.<br>

---

![4](/images/in-schools/digital-maker/projects/a-better-world/traffic-light-sensor/traffic-light-sensor1.jpg)

**6. Place sensors and buzzers within restricted area**<br>
Designated Restricted Area near the road. The sensors and buzzer will be placed within the restricted area.<br>

---

**7. Test on red sensor**<br>
When it is Red Man, the sensor will be turned on and the LED light will be automatic lighted.<br>
When someone steps into the designated restricted area, the sensor will trigger the LED light to blink, the buzzer to sound and the warning message “Stay Clear” to show up.<br>

---

**8. Test on green sensor**<br>
When it is Green Man, the sensors will be turned off.<br>

---

**9. Technical Instructions of the Project**<br>
**Inputs**<br>
Button A = Green Man<br>
Button B = Red Man<br>
P2 = Echo (Signal input pin)<br>

**Outputs**<br>
P0 = Buzzer<br>
P1 = LED strip<br>
P4 = Trig (Signal output pin)<br>
P5 = Button A<br>
P8 = Red LED (indicate Red Man)<br>
P11 = Button B<br>
P12 = Green LED (indicate Green Man)<br>

**Variables**<br>
Push Button 1 → To store (indicate) if it is Green Man or Red Man now. If the value is 0, then it is Green Man. If the value is 1, then it is Red Man.<br>

Light Sensor → To store the distance of an object from the ultrasonic sensor.<br>  

**Notes**<br>
Ultrasonic sensor uses sound waves to measure the distance of an object. The sensor outputs (P4) a sound wave and it will be reflected back to the sensor’s inputs (P2). After the sound wave is sent out, the sensor will time how long it takes for the reflected sound to get back to the ultrasonic sensor.<br>

---

![5](/images/in-schools/digital-maker/projects/a-better-world/traffic-light-sensor/traffic-light-sensor4.jpg)

**10.  Initialization**<br>
● Set P1 = 0 is to turn off all LED strip<br>
● Set buzzer to rest at 1/8 beat<br>
● Set Push Button 1 to 0 is to set everything to Green Man.<br>

---

**11.  Run forever loop continuously**<br>
If Button A (Green Man) is pressed, do the following:<br>
● Set variable Push Button 1 to “0”<br>
● Set Buzzer to rest at 1/8 beat<br>
● Turn on Green LED by setting P12 to “1”<br>
● Turn off Red LED by setting P8 to “0”<br>

If Button B (Red Man) is pressed, do the following:<br>
● Set variable Push Button 1 to “1”<br>
● Turn on LED strip by setting P1 to “1”<br>
● Turn off Green LED by setting P12 to “0”<br>
● Turn on Red LED by setting P8 to “1”<br>

If it is Red Man, do the following:<br>
● Turn on the ultrasonic sensor and returns the distance in cm.<br>
● Store the distance in the lightSensor variable.<br>
● If the lightSensor variable is between 0 and 9, then repeat the following 3 times.<br>
o Turn on LED strip by setting P1 to “1”<br>
o Sound the buzzer and pause for 20 ms<br>
o Turn off LED strip by setting P1 to “0” (this is to create the blinking effect)<br>
● If the lightSensor variable is not between 0 and 9 (else statement), do the following:<br>
o Continue to turn on LED strip by setting P1 to “1”<br>

If it is not Red Man, do the following:<br>
● Clear everything.<br>

---

**12.  Project complete!**<br>
If it is Red Man, do the following:<br>
● Turn on the ultrasonic sensor and it returns the distance in cm.<br>
● Store the distance in the lightSensor variable.<br>
● If the lightSensor variable is between 0 and 9, then repeat the following 3 times.<br>
o Show “STAY CLEAR” in microbit screen.<br>

---

Click [here](/in-schools/digital-maker/projects/) to go back to the Digital Maker Projects By Community main page.
