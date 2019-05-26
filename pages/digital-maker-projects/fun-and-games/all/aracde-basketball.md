---
layout: simple-page
title: Arcade Basketball
permalink: /arcade-basketball/
breadcrumb: Arcade Basketball
---

Stephen Curry, Kobe Bryant, Lebron James, what do these people have in common? You guessed it, Basketball! In this project, build your very own arcade basketball game with micro:bit! A great game be it with your friends or family, you'll be the life of the party! So let's begin coding and building the arcade basketball game!

![1](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball1.png)

**You will need**

[Block Editor Link](https://makecode.microbit.org/)
[Hex File Download](https://www.dropbox.com/sh/cj6uj8lo7pownms/AACYJpCFwbQx9HYWlBgehA_Ma?dl=0)
[Coreldraw Link](https://www.dropbox.com/sh/cj6uj8lo7pownms/AACYJpCFwbQx9HYWlBgehA_Ma?dl=0)

---

1x BBC micro:bit<br>

1x micro USB cable<br>

1x AAA battery cage<br>

2x AAA batteries<br>

1x IR sensor<br>

1x Roll of double-sided tape/mounting tape<br>

1x Glue gun/wood glue<br>

 Play Dough<br>

1x Plastic cup<br>

1x Penknife<br>

3x Toilet paper roll<br>

5x Alligator clips<br>

5x Wood planks size 20x30cm<br>

decoration materials<br>

3D Printer<br>

---

#### Instructions

![2](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball2.png)

**1.  Dimensions for Wood Planks** <br>Use Inkscape or CorelDraw to design the cutting outline of wood planks. Link to CorelDraw design file will be provided in the captions below.<br>

---
![3](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball3.jpg)

**2.  Cutting of Wood Pieces** <br>Now we can prepare the 4 pieces of wood planks of size 22cm x 30 cm. Use a laser cutter or saw to cut out the outline from the wood planks. Pictures of the different wood pieces will be shown on the right.<br>

---
![4](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball4.jpg)

**3. Assembling Wood Pieces** <br>Use wood glue to assemble the wood piece together to form the arcade station.<br>

---
![5](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball5.jpg)

**4. Completed cut wood pieces**<br>Congrats! You now have a basketball court frame! The basketball court should look like the image on the right.<br>

---
![6](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball6.jpg)

**5. Making Bottom Surface of court**<br>Use a pen knife/scissor to cut a rectangular shaped cardboard at 28x18cm. This cardboard will act as the bottom surface of the station.

Take 2 toilet rolls, and cut them into 3 rolls at the height of 4.5 cm. They serve as the supporting part of the bottom surface.<br>

---
![7](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball7.jpg)

**6. Place bottom surface into frame**<br>Place the 3 toilet rolls in the centre of the frame and place the rectangular cardboard over it. The cardboard should be slanted to allow the basketball balls to slide downwards.<br>

---
![8](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball8.png)

**7. Assembling the hoop (Pt.1)**<br>We'll now begin making the basketball hoop by using cardboard and a recycled plastic cup.

Cut a square from cardboard of size 8x8 cm and 4 rectangular strips of size 3x6 cm.<br>

---
![9](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball9.jpg)

**8. Assembling the hoop (Pt.2)**<br>Use a glue gun to assemble the 4 rectangular strips into a tube like the picture on the right.<br>

---
![10](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball10.jpg)

**9. Assembling the hoop (Pt.3)**<br>Glue the tube together with the square board. Use screw driver to punch through holes at the 2 opposite sides.<br>

---
![11](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball11.jpg)

**10. Assembling the hoop (Pt.4)**<br>Using a pair of scissors, cut away half of the bottom of the cup and 2 holes at the side.<br>

---
![12](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball12.jpg)

**11. Assembling the hoop (Pt.5)**<br>Use a pair of scissors to cut 2 holes at the side of the plastic cup, insert a cable tie through the cup from the 2 holes.

Secure the cup with the cable tie with the basketball board.<br>

---
![13](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball13.jpg)

**12.  Pathway for basketball**<br>Next, measure the size of the cup and cut a cardboard piece which can be fitted into the cup. Attach the cupboard piece into the cup to form a slanted surface and secure well with tape. This structure is to ensure a smooth pathway for the basketballs as they fall through the cup.<br>

---
![14](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball14.jpg)

**13. IR Sensor Placement**<br>Place the IR sensor at the bottom of the cup. Secure the sensor position with mounting tape.<br>

---
![15](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball15.jpg)

**14. Completed Basketball Frame**<br>With this we have made the structure basketball board and hoop. Use mounting tape to tape this part to the wooden basketball station.<br>

---
![16](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball16.png)

**15. Coding of the micro:bit (Pt.1)**<br>For the first part of the program, we are using “running time” to set up a timer of 20s. During the running time of the timer, micro:bit will read the input signal from the IR sensor. The IR sensor will send out signal 0 when it is sensing. IR sensor will be connected to Pin1 in this project. When Pin1 reads 0, score will go up by 1. micro:bit will display the score at the same time.

After the timer stops, micro:bit shows “GAME OVER”, and the score of the game. If the high score is being broken, micro:bit will play a melody and prompt the player that a new high score has been created.

Refer to Ingredients for links to Block Editor and Hex File.<br>

---
![17](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball17.png)

**16. Coding of the micro:bit (Pt.2)**<br>For the next part of the code, we will program the B button to display the current high score. The score can be obtained anytime throughout the game.<br>

---
![18](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball18.png)

**17. Download Code to micro:bit**<br>Download hex file (above) of the program and save it to micro:bit. Fix the microbit to the basketball game frame. 

Now we can wire the circuit up using 3 jumper wires with 3 alligator clips attached to it

1. Connect a 9V battery to the IR sensor.<br>

2. Power the micro:bit with 2 AAA batteries.<br>

3. Connect the output signal of the sensor to micro:bit Pin1.<br>

4. Connect the Ground of the sensor to the micro:bit GND.<br>

5. Connect the top part of the speaker ear jack to Pin0 on micro:bit, and bottom part connect to GND.<br>

---
![19](/images/in-schools/digital-maker/projects/fun-and-games/arcade-basketball19.jpg)

**18. Time to Play!**<br>Well done! You've completed the project! You can use either play dough to make the basketball balls or 3D print them. 3D print file will be provided in the caption below.

Start playing with your friends by throwing the balls into the hoop, and see who gets the high score! Using the micro:bit and the attached IR sensor, you're now able to track your scores!<br>


Click [here](/in-schools/digital-maker/projects/) to go back to the Digital Maker Projects By Community main page.
