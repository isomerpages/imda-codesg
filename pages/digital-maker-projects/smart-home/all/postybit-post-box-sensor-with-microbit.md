---
title: 'Posty:bit - Post Box Sensor with micro:bit'
permalink: /postybit-post-box-sensor-with-microbit/
breadcrumb: 'Posty:bit - Post Box Sensor with micro:bit'

---

**Contributed by Ferry Djaja**

![1](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybitmain.jpg)

Posty:bit is a post box monitoring system that is built with micro:bit. It has two smart modules that are interacting with each other.<br>


**You will need:**<br>

<a href="https://makecode.microbit.org/" target="_blank">Code the micro:bit</a> 

2 x micro:bits<br>
2 x battery holders<br>
4 x AAA batteries<br>
2 x USB connectors<br>
1 x PIR sensor (SEN-02046 or DYP-ME003)<br>
3M double sided tape<br>

#### Instructions

![2](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit1.jpg)

**1.  Transmitter and Receiver** <br>
**Transmitter**<br>
We need to put the Transmitter in your mail box to monitor any incoming mail from the postman. It has a PIR sensor to detect any movement in the box. You need to put the Transmitter on one of the side inside the box. See Installation section for more details.<br>

**Receiver**<br> 
You need to carry a Receiver in order to check your mail box. Once you pressed the button A on the micro:bit, it will check if there is a mail in your box and it indicates the above LED status:<br>

---

![3](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit2.jpg)

**2.  Build The Transmitter** <br>
Because our PIR sensor runs at 5V, we need to do some hacking to work with micro:bit. Remember micro:bit input voltage is 3.3V.<br>

Instead of using the normal VCC 5V pin, we will use the VCC 3.3V pin as highlighted in point A. The final connectivity is shown in the above picture.<br>

---

![4](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit3.jpg)

**3.  Attaching the PIR sensor** <br>
Hook up the PIR sensor to the micro:bit as shown in the image.<br>

---

![5](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit4.jpg)

**4.  Adjust the sensitivity of PIR sensor** <br>
We need to adjust the sensitivity and time delay on the PIR sensor. Turn both orange dials anti clockwise as far as they will go. This will set the motion sensitivity to its least sensitive setting and time delay between sensing the shortest possible interval.<br>

---

![6](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit5.jpg)

**5.  Build The Receiver** <br>
As there is no external component attached to the Receiver, actually there is nothing to build, it is only the micro:bit itself that you need carry in order to check your mail !!. As an illustration, you can attach the receiver onto your bag (like the below picture). The bag will tell you if there is a mail!<br>

---

![7](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit6.jpg)

**6.  Upload the HEX file onto the JavaScript Block Editor** <br>
I have attached the Transmitter and Receiver HEX files above, so you can learn the logic and may modify to enhance the functionality. For those of you who do not wish to learn how to code is written, you may just download the HEX files and transfer it onto your micro:bits, and skip to Step 11.<br>

For those of you that are interested in the code, upload the HEX file onto the Javascript Block Editor by clicking on the “Open Projects” tab and point the code editor to import the HEX file. Move on to Step 7.<br>

---

![8](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit7.jpg)

**7.  Explanation of how Transmitter works** <br>
The Transmitter has a PIR sensor attached to digital pin P01.<br> 

The program is keep monitoring in-cycle the value of digital pin P01, if the value is high (1) - assuming the mail is in the box, it will notify the Receiver on the incoming mail from the postman by sending a certain value via the radio frequency group 18.<br>

Notice that variable mail = 1 indicates mail has arrived, mail = 0 indicates no mail. If the radio receives receivedNumber= 3, it acknowledges the user has checked the status (the button A on the receiver was pressed).<br>

If the radio receives receivedNumber = 4, it will tell the Receiver that Transmitter is still alive. This is important to make sure the Transmitter is working as expected.<br>

---

![9](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit8.jpg)

**8.  Explanation of how Receiver works** <br>
The Receiver has a radio function on the group 1 that monitors the incoming values from the Transmitter.<br>
If receivedNumber = 1, indicates the mail has arrived (mail = 1)<br>
if receivedNumber = 2, indicates no mail (mail = 2)<br>
if receivedNumber = 5, indicates Transmitter is still alive and within range (batt = 1)<br>

---

![10](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit9.jpg)

**9.  Overall explanation for how PostyBit works** <br>
Within ![10a](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit9a.jpg) block:<br>

Check if Transmitter battery has gone  flat or out-of-range and let user know by showing the LED status:<br>
![10b](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit9b.jpg)<br>

Check if the mail is in the box and let user know by showing the LED status:<br>
![10c](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit9c.jpg)<br>

---

![11](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit10.jpg)

**10.  Overall Explanation of how PostyBit works - Part II** <br>
Within ![11a](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit10a.jpg) block:<br>

If there is no mail, let user know by showing the LED status:<br>
![11b](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit10b.jpg)<br>

Do a ‘ping’ to Transmitter to make sure it is alive and responding.<br>

---

![12](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit11.jpg)

**11.  Let’s upload the program to micro:bit!** <br>
You need to download each program for transmitter and receiver and upload to micro:bit. Click done once you see the below screen, it means the script has been successfully generated and downloaded to your default download folder.<br> 

Drag the downloaded script for transmitter and receiver and drop it onto your micro:bit drive. The downloaded script should end with a  .HEX extension. We will have two HEX files, one is for transmitter and the other one is for receiver.<br>

---

![13](/images/in-schools/digital-maker/projects/smart-home/postybit-post-box-sensor-with-microbit/postybit12.jpg)

**12.  Install the Transmitter** <br>
Put your Transmitter in your mail box in such a way if the postman put the mail in your box, the PIR sensor can detect. I use double-sided tape on the back of the wood and stick the Transmitter as shown in the below image.<br>

---

**13.   Project Complete!** <br>
Well Done! Project Complete !!!<br>

Did you enjoy making this project?<br>

---

Click [here](/in-schools/digital-maker/projects/) to go back to the Digital Maker Projects By Community main page.
