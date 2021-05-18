---
title: 'bitLocker - microbit Front Door Security System'
permalink: /bitlocker-microbit-front-door-security-system/
breadcrumb: 'bitLocker - microbit Front Door Security System'

---


**Contributed by Ferry Djaja**

Now you can build the front-door security system equipped with door sensor and alarm. Anyone is trying to force to open the door will trigger the alarm!!<br>

The only way to disarm or deactivate the alarm is to key in the correct 4-digit PIN numbers. In this tutorial, you will learn and create the bit:Locker – micro:bit Front Door Security system with two electronic components: buzzer and magnetic door sensor, microPython and of course: micro:bit!<br>

What happen if the micro:bit is out of power or someone has removed the battery? Do we need to re-enter the PIN again? Don’t worry, micro:bit can still remember the PIN that was entered.  And user can also reset the PIN once they entered the correct PIN numbers.<br>

Let’s start to build!!<br>

**You will need:**<br>

1 x micro:bit<br>
1 x battery holder<br>
2 x AAA batteries<br>
1 x Buzzer<br>
1 x Magnetic Contact Switch (door sensor)<br>
2 x alligator clips with wires<br>

#### Instructions

![1](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker1.jpg)

**1.  Setting up the environment** <br>I am using the microPython to develop the program, so we need to download the microPython Mu editor. Go to <a href="https://codewith.mu/" target="_blank">Code with Mu</a> and click “Download now”.
 
Select the Mu editor according to your operating system. For my case, I am using Windows, so I will download the Mu for Windows.<br>

---

![3](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker2.jpg)

**2.  Opening up Mu Python Editor** <br>Once you have downloaded, double click the executable file, and you will get the Mu Python Editor opened like in the image shown.<br>

---

![4](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker3.jpg)

**3. Connecting the Buzzer and Magnetic Sensor to micro:bit** <br>Connect the buzzer and magnetic door sensor as per the above diagram. Take care of the buzzer pin, connect the pin that is labelled + to pin 0 of micro:bit<br>

---

**4. How to use bit:Locker**<br>Set the PIN first

* You will see the sign “S” indicated on the LED matrix. We need to set the 4-digit PIN first.  “S” means to set the PIN numbers.<br>
* Press button A to select the number you wish to enter. The number on the LED matrix  is your PIN digit number. Every time you press the button A, the number will increase. If the number turns to 9, it will be set to 0 again. You can choose any number from 0 to 9 as your PIN.<br>
* Press button B to enter the number that you have selected. You need to do it four times as the program needs the 4-digit PIN numbers.<br>
* Once you have entered the four digit numbers, program will ask user to confirm by showing the scrolling text “Confirm?” on LED matrix. Press A button to confirm or press B button to cancel and re-enter the PIN again.
Once you have done it, you will see the sign “E” on the LED metrics. “E” means it is ready for user to enter the PIN numbers.<br>

Enter the PIN<br>

* Enter the pin to disarm the alarm.<br>
* Press button A to select the PIN number, press button B to enter. You need to do it four times, if the PIN you have entered is correct, you will see the smiley icon displayed on the LED matrix and eventually the heart sign. It means the alarm has been deactivated and now you can freely open the door.<br>

---

![5](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker4.jpg)

**5. How to use bit:locker - continued**<br>See the table to reference what the symbols on the LED matrix mean.<br>

---

![7](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker5.jpg)

**6.  Understanding the logic**<br>I have uploaded the python code to GitHub, so you just can download and upload to your Mu editor. Click <a href="https://github.com/ferrygun/bit-locker" target="_blank">here</a> to go to the code.<br>

---

![8](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker6.jpg)

**7. Understanding the code: Main()**<br>On the Main function is just a forever loop where the code is always checking if the door sensor is open while the alarm is activated. We need to check the value of the analog pin p0, if the contact is closed, the value will always 3, if the contact is opened, the value will vary and it will be more than 3.<br>

---

![9](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker7.jpg)

**8. Understanding the code: SetSecretPin()**<br>This part of the code is to set the PIN from the initial stage if the PIN has not been setup and to store the entered PIN in the Local persistent Filesystem that we are going to touch in the subsequent steps.<br>

---

![10](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker8.jpg)

**9. Understanding the code: SetSecretPin() - continued**<br>If the program has received the 4-digit PIN numbers, it will ask user for the confirmation. Once user has confirmed (by pressing the button A again), the PIN will be stored in the persistent FileSystem so micro:bit can remember the PIN even if the power is down.<br>

---

**10. Understanding the code: Local Persistent File System**<br>Micro:bit has a small file system to store the program when you flash your program. When the micro:bit is running, you can read, create and delete the files. The flash memory in micro:bit is persistent that means any data you stored, it will be available when the micro:bit is switched off and on though.

With that in mind, we need to design the bit:Locker to remember the PIN that was entered by the user during the PIN setup process. For this case, I am using the Local Persistent File System to store the PIN data in a persistent manner so it will remains intact between restarts of the device. Here is the piece of code to handle that:<br>

![11](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker9.jpg)

---

![12](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker10.jpg)

**11. Understanding the code: Local Persistent File System - continued**<br>I created the filename secret.txt to store the PIN in the form of array on the micro:bit. Once the file has been created, you can check from the Mu editor by clicking the Files menu and you will see the filename on your micro:bit.<br>

---

![13](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker11.jpg)
**12. Understanding the code: GetUnlock(p)**<br>This part of the code compares the PIN that was stored earlier with the PIN that was entered by the user. If the PIN is match, the alarm will be deactivated. We also play some music with buzzer on pin 0 on the  micro:bit to attract attention and make it more interesting :)<br>

---

![14](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker12.jpg)
**13. Understanding the code: GetUnlock(p) - continued**<br>Refer to the flowchart for further explanation.<br>

---

![15](/images/in-schools/digital-maker/projects/smart-home/bitlocker/bitlocker13.jpg)
**14. Understanding the code: Global Variables**<br>And finally, to link the status between all the functions, we need to have the global variables. We need to write some functions to set and get the value of global variables in microPython.<br>

---

**15. Demo video on YouTube and idea for improvement**<br>With this, we come to the end of our program. Below are some video resources of the project for your reference:

 
Demo on how to use bit:Locker:.<br>
<div class="bp-youtube">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/52AHtYndh7w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
<div class="bp-youtube">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/gK1MqeqcFhY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

Click [here](/in-schools/digital-maker/projects/) to go back to the Digital Maker Projects By Community main page.
