---
layout: project
type: project
image: images/micromouse_cover.jpg
title: Micromouse
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2017-8-23
labels:
  - Robotics
  - PIC Microcontroller
  - C
summary: My team designed and built an autonomouse stepper-motor mouse with the ability to traverse through a 16 x 16 maze
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse.png">
  <img class="ui image" src="../images/micromouse_circuit.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

In this project, my main job was mainly in the programming apsect. However, I did help with measuring the frame of our mouse through autoCAD and getting it machined. We used MPLAB X as our IDE and used the Pickit 3 to program our PIC microcontroller. I helped with programming our FloodFill algorithm. We used different algorithms to solve the maze, such as left and right wall huggers, however, floodfill was what we ultimately wanted to use. We completed the FloodFill algorithm and put it in the mouse. We got 2nd place in the Fall 2017 competition.

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).



