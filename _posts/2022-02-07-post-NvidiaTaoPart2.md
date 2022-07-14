---
title: "Part 2: Classification"
date: 2022-07-02T15:34:30-05:00
categories:
  - blog
tags:
  - Computer Vision 
---

Part1: Introduction to Nvidia Tao <br />
Part2: Classification <br />
Part3: Object Detection <br />
Part3.1: Object Detection(DetectNet_v2) <br />
Part3.2: Object Detection(SSD) <br />
Part3.3: Object Detection(Yolo)<br />
Part4: DeepStream deployment<br />


Nvidia Tao is much related to computer vision tasks alone. In computer vision classification is the primary task to proceed with. So lets begin with that.

### Important Note:

>  I am using a virtual machine(ubuntu 20.04) for my tasks, so I have to do things from terminal alone, so I will not be using the jupyter notebook.

>  I will recommend using the tmux package in the terminal, because my virtual machine can get disconnected and then I running terminal can be gone, so I suggest start using a tmux terminal, so that if connection is lost even, you can login and still attach to the specific session.



## Classification Task

I am using the mask detection dataset from [kaggle](https://www.kaggle.com/datasets/prithwirajmitra/covid-face-mask-detection-dataset). My moto is to detect the if the person is wearing mask or not. 







As I have told you in the part 1 blog, lets write the config file for training 