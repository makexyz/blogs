---
layout: post
current: post
cover: https://i.ibb.co/1qrjy32/Cover.png
navigation: True
title: 9g Micro RC Servo Robot Arm
date: 2020-05-27 21:00:00
tags: arduino
class: post-template
subclass: 'post'
logo: assets/images/ghost.png
author: deadblox
---

Today, I'll share a really old project that I followed - A 9g Micro Servo Arduino Robot Arm.

<iframe width="560" height="315" src="https://www.youtube.com/embed/3SC-O6A-700" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

This project was born around October 2016. At the time, it was not created by an original idea, it was actually a combination of the idea of ​​hardware and software from two different projects that I credit below. However, this product was redesigned in terms of structure, circuit, and program to be more complete than the previous two products. With the frame designed and printed in 3D to optimize the installation of 9g RC Servo motors as well as firmer, the electrical part was designed into Shield that could be installed on existing Arduino Uno, the program was also been modified to retain only those components that are truly necessary and optimized for control speed.

As a result, you have a robot arm that can be taught by manipulating resistors on the shield for each position of the joints. Each time you teach a robot a new location, you will save the location data (actually the value from the potentiometer) into the Arduino in chronological order. After teaching the robot all the moves, you can switch to Play mode so that the robot repeats all operations in order and always on the time between location changes. The best thing about this project is the Arduino code that was inherited from Pinaut's project. If you pay close attention, you will see all the Micro RC Servo reaching the destination at the same time even though the angle is different. This makes the smoothness of this robot model and Pinaut's robot model that few other RC Servo models have.

Thanks for reading,
If you like my videos, please like and subscribe to [my channel](https://www.youtube.com/channel/UC4v28AauStqzl2rwNGl9QcA).

Credits:

1. [Micro Servo Robot - Pinaut](https://www.youtube.com/watch?v=bLnAJ-mSElE)
2. [LittleArm - V1](https://www.kickstarter.com/projects/slantrobotics/littlearm-v3-mini-arduino-robot-arm-for-stem-and-hobby)
