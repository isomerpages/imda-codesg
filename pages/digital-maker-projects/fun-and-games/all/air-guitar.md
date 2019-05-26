---
layout: simple-page
title: Air Guitar
permalink: /air-guitar/
breadcrumb: Air Guitar
---

![1](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar1.jpg)

We've all heard of the game, Guitar Hero, whereby players use a guitar-shaped game controller to simulate an actual guitar. In this instructable, we'll teach you how to make your very own customisable guitar controller paired with micro:bit! You'll never have a silent moment again in the house! So let's get started!

**You will need:**

[Block Editor Link](https://makecode.microbit.org/)<br>
[Hex File Download](https://www.dropbox.com/sh/cj6uj8lo7pownms/AACYJpCFwbQx9HYWlBgehA_Ma?dl=0)<br>

---

1x BBC micro:bit<br>

1x micro USB cable<br>

1x AAA battery cage<br>

2x AAA batteries<br>

 1x Mini Speaker<br>

1x Roll of double-sided tape/mounting tape<br>

1x Glue gun<br>

1x Ruler<br>

1x Penknife<br>

3x Pairs of wooden chopsticks<br>

2x Alligator clip wires<br>

2x Set of screws and nuts<br>

copper tape<br>

decoration materials<br>

cardboard<br>

3D Printer<br>

---

#### Instructions

![2](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar2.jpg)

**1.  Cutting Outline of Air Guitar** <br>Use a penknife/scissors to cut cardboard into 2 pieces of guitar shape, and 3 side straps. Dimensions are given for reference.<br>

---
![3](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar3.jpg)

**2.  Glue Side Straps to add Height** <br>Bend the side straps on the edge of one guitar body, and glue them together. Once done, glue the other guitar shape piece on top to get a full bodied cardboard guitar frame.<br>

---
![4](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar4.jpg)

**3. Attach Guitar Neck** <br>Next, we will make the neck of the guitar. Cut out 2 straps of the neck piece at dimension of 28x4cm. Put 3 pairs of wooden chopsticks in between the 2 straps, and glue them together. This is to provide a strong support for the guitar neck.<br>

---
![5](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar5.jpg)

**4. Cut slot for Guitar Neck**<br>Cut out the body top cover of 5x3.5 cm, and cut a slit of 4x1.5cm in the centre to slot in the neck later.<br>

---
![6](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar6.jpg)

**5. Attach**<br>Glue the cover on the top of the guitar frame. The product should look like the picture on the right.<br>

---
![7](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar7.jpg)

**6. Slot in Guitar Neck**<br>After slotting in the neck portion, you may apply glue for added reinforcement. Product should look like the picture on the right.<br>

---
![8](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar8.jpg)

**7. Design and Print**<br>Cut 2 identical pieces from the cardboard to form a guitar head, and glue them together. Insert the head into the guitar neck, and glue the connecting edge between the neck and head. You'll now have a finished guitar design. Start decorating it with your art materials!<br>

---

**8. Coding the Program**<br>In this step, we will code the Micro:bit in Block Editor. You can access the block editor from the captions below. In this project, we will program the guitar to play some pre-programed melodies by pressing onto buttons and changing its pitch by tilting the guitar in certain angles.

Begin by coding an unique starting screen, this screen will appear when the micro:bit is powered on.<br>

---
![9](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar9.png)

**9. Setting Melodies**<br>Next, we can program the Micro:bit to play different melodies when pressing either Button A or B. We've programmed button A to play “We Will Rock You” when pressed while button B plays “Let It Go” (Frozen).The images on the right will show the codes required for both button A and B. Feel free to create your own song if you wish to!<br>

---
![10](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar10.png)

**10. Final Coding Step**<br>Let's make a mode whereby Micro:bit produces a sound when tilting. This mode will be triggered by pressing on Pin1. Rename a variable "pin1" to read the analog signal from Pin1, and this variable will decide if Pin1 is pressed.

In this project, the pitch is controlled by the light level and it is detected by the Micro:bit in-built light sensor.

We can code the Micro:bit to plot graph according to the light level as well.<br>

---
![11](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar11.png)

**11. Transfer code into Micro:bit**<br>After all the coding is done, we can use the simulator on the left to try out all the functions we have programmed. Plug in the micro:bit to your computer, download the script and copy it onto the micro:bit. Copy the downloaded script to your micro:bit drive. The downloaded script ends with a .hex extension.<br>

---
![12](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar12.jpg)

**12.  3D Print Micro:bit Cover**<br>In this step, we are going to 3D print the Micro:bit cover.

The link for the 3D design will be in the captions below. After you download the model, use your 3D printer to print them out.The final Micro:bit cover should look like the image on the right.

[3D Design Print File](https://www.tinkercad.com/things/aeMZ5LLeGmQ-imda-microbit-cover-for-air-guitar)<br>

---
![13](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar13.jpg)

**13. Connect Micro:bit to audio speaker**<br>Place the programmed Micro:bit into the printed cover, and use a pair of screw and nut to secure the cover. Connect the Micro:bit with batteries. Take 2 alligator clip wires to connect Micro:bit with the audio cable of mini speaker. You can refer to the image on the right if you're unsure of the wiring.<br>

---
![14](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar14.jpg)

**14. Extend Pin1 onto Guitar Neck**<br>In order to press Pin1 easily, we can extend Pin1 out to the guitar neck. Use a long strap of aluminium foil, and tape in from the guitar to the neck.

Paste conductive copper tape on the top of the aluminium foil, paste one end to Pin1 on Micro:bit. In this way, you press Pin1 by pressing the copper tape on the guitar neck.<br>

---
![15](/images/in-schools/digital-maker/projects/fun-and-games/air-guitar/air-guitar15.jpg)

**15. Complete**<br>Andddd you're done! You now have your very own Micro:bit Air Guitar. Go forth and test the capabilities of it! Have fun!<br>


Click [here](/in-schools/digital-maker/projects/) to go back to the Digital Maker Projects By Community main page.
