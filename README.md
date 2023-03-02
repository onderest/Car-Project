# School project - Autonomous car - ELA21, YRGO

![alt text](https://github.com/onderest/Car-Project/blob/main/Fig1.png?raw=true)

Fig.1 - Our two competing cars and trophy, first and second place!!! 

## Introduction

Every year YRGO holds a competetion as a school project where the two electronics engineering classes are split in grops four groups for each class where each group is to design an autonomous car. The car is meant to race three other cars at once on a track where the one who completes to most laps in 3 minutes is the winner. There are two groups in the group stage and than quarter, semi and finals. So alot of races which means alot of things can go wrong!



Our goal was ofcourse to win, and our strenths was moore towards hardware than software so we choose components based on what we felt comfotable programming, Arduino Nano, three analog distans sensors that worked in the area of 8-80cm, which suited the track well, and a servo with a very detailed datasheet, and lastly a regular brushed dc motor.
With easy acces to 3D printer we also choose the car "summon swift" becouse it was very easy to costomize and replace parts or fit new parts on it's chassi.

We wanted to write the code in C++ as it had some advantages with classes instead of using structs in C, even tho we never wrote C++ befoure! But you have to have some challanges in every area. 


## The Build

We first wrote some test codes just to se that we could get the critical parts to work properly (servo, sensors and motor). After that we started to design our curcuit board for our H-Bridge, and a platform for the car for easy mounting of components and slim fit as we wanted to be able to still mount the bodywork for good looks!

![alt text](https://github.com/onderest/Car-Project/blob/main/Fig2.png?raw=true)

Fig.2 - Platform and Curcuit board for H bridge and Arduino.

When the car was complete and ready for our first test, it worked, but not good... The servo was not working properly and jumping all over the place. This was due to two or three reasons, our code, and lack of current, and maybe that the Arduino was to slow to control everything at once. The servo was wired thru the Arduino but needed about 1A, nowhere near what the Arduino could output. Our solution was a 5V LDO directly from the battery to the Servo. The secound problem was with the code, this was harder and as time was running out and frustration getting higher, we descided to write an identicle code in C, and it worked perfectly! The problem was that Destructors in our C++ code was called during at times and we couldn't figure out why, nor could our teacher.

![alt text](https://github.com/onderest/Car-Project/blob/main/Fig3.png?raw=true)

Fig.3 - Left picture is the servo PWM without load, and right is with servo connected, not good.

During this time we also found out that we were allowed to enter two cars to the competition, and as we had a spare car that was ment to be used for spare parts we descided to build another one, so we could enter with one car each (Team of two). 
Since we already needed to design a new board for the secound car, we descided to go for two Arduino boards to solve the third problem. 
Now we would have one board for the motor and forward analog sensor for forward/reverse operation. And one board for the servo and the two side facing sensors that controlled whitch way to turn.

![alt text](https://github.com/onderest/Car-Project/blob/main/Fig4.png?raw=true)

Fig.4 - Left picture is the secound card for the first car to control the servo, right picture is one card for the new car.

After theese changes our cars worked perfectly and we could spend the last 2 weeks optimizing the cars for the track, trying diffrent motors and angels for the sensors. And ofcourse adjusting PID for the steering.

And on race day we set a new all time lap record with 18 laps and ofcourse taking first and secoond place means this was not just luck! very happy with the result and our cars after all the time we spent on this project!
