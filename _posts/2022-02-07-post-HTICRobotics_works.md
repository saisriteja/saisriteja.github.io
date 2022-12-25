---
title: "Life at HTIC: The place I started to learn things."
date: 2022-07-02T15:34:30-04:00
categories:
  - blog
tags:
  - Personal
  - HTIC
  - Robotics
---


# Intro
HTIC is a health care research lab inside IIT Research park. I have joined in the Team SSR(spine surgical robotics) as a final year intern. I have worked for almost a year and half over here as a robotic engineer. The lab is run by the professor Dr. Mohanasankar Sivaprakasam. When I go to the lab, I see a lot of unique minds wanted to do something different. 


# Professional Life
I was working all the time, under the guidance of a MS Scholar named Shyam A. The perk I got working in the team is the flexibility to learn something new in the first couple of months. I always had a soft corner of healthcare applications and products. So I was working on sundays, back in those days. The first couple of months I got to learn about working in ROS and packages along with it(MoveIt, FastIK, RViz). This is like full time things, which is so exiting to see you working robotics in simulation and stuff. 

The perk of being in office and working is you can start moving with the real robot. I have personall worked with 4 different robots, namely, Elfin, UR, KUKA and Staubli. I have worked with both Cobot and Industrial robots. The company has enough fund to bring in and spend for new robots, It doesnot purchase all of them, but the company rents. Yet a few robot, the company owns it.

So after working with robots for 6 months, I started digging into application part. I was given the task to design the motion planning of the robot for spine surgical application. We already have a motion planning code, but we wanted it to be fast and the code to be feasible to adopt for more robots. 


| ![space-1.jpg](/assets/images/htic_robot/20211027_204352.jpg) | 
|:--:| 
| *Robots in HTIC(2021).* |

| ![space-1.jpg](/assets/images/htic_robot/IMG-20170818-WA0001.jpg) | 
|:--:| 
| *Me and Shashank in love with robots(2016).* |



## Building the core product
The application is simple, imagine drilling a needle into the wall with bare hand. you see the needle can tumble and going in wrong direction. Here doctors do the same thing, but in a spinal chord. Since spine is connected to brain, it the needle insertion is not accurate, things go bad. Imagine you have a holder like an extra arm to hold the screw driver, all you need is to rotate it. The one which holds the driver is the robot here. This is what robot does, simply comes and holds the screw driver for the doctor.


| ![space-1.jpg](/assets/images/htic_robot/spirnrobt.jpg) | 
|:--:| 
| *Robot holding the tool to drill the pedicle screw into the vertebrae.* |


Take a clean look at the picture, seems simple right, but not, one major enemy is collision during planning, we dont have a lot of cams, around, the robot should plan the trajectory using IR markers.
Collision include
1. Robot - Needles on the body
2. Robot - Robot
3. Robot - Doctor
4. Robot - Patient

We need to track all of them and do motion planning, so we built softwares that can replicate the real time simulation inside RViz and used the collision libraries to check. We have checked the collisions and them made proper collision free trajectory.I have helped my peer Aswath Govid, to write motion planning software. 

| ![space-1.jpg](/assets/images/htic_robot/docs.jpg) | 
|:--:| 
| *The surgical site, have look around the room.* |

Even I was working with really good robots and people around, somewhere deep down I wanted to work with Images and Neural Nets. Everytime when some says it the desire to work with it grew stronger, right at that moment I have got an oppurtunity to work with Detect Tech as a CV-Deep Learning Engineer-I. 


## KUKA Competition
We have applied for one of the world best robotic competitions, the annual KUKA robotics competition. We are one of the top 5 finalists in the end. 



## Expo
I have went to an expo, to checkout what other robotic companies are upto.
| ![space-1.jpg](/assets/images/htic_robot/20211212_163224.jpg) | 
|:--:| 
| *Robotics Expo.* |

# Personal Life

Along with software engineers, there is a mechanical team and imaging team. My peers in those teams are so good to me and took good care of me when I needed. A special thanks to Nivas and Pradeep. 

Being my first job, the people are of various ages, when I joined, I was the youngest. So all my peers who are elder than me took responbility to teach all the things.

When it comes to professional things, Shyam is a good mentor, but Minhas was one who taught me all the other stuff. Dear Minhas, as your disciple, I forever owe you. Thank you for all your teachings. 

| ![space-1.jpg](/assets/images/htic_robot/IMG_0571-COLLAGE.jpg) | 
|:--:| 
| *Anthony, Me, Nivas, Minhas, Aswath(top photo). The only people you need to make life happier.* |


| ![space-1.jpg](/assets\images\htic_robot\20220204_212123.jpg) | 
|:--:| 
| *You gotta party when you are in world top 5.* |





