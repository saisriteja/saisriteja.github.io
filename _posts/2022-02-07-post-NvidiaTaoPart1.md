---
title: "Part 1: Introduction to Nvidia Tao"
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



You could have listen to pytorch or tensorflow when you enter in the world of Machine Learning. These are the two important frameworks that are currently the best for implementation any deep learning model. __

One would prefer tensorflow when it comes to deployment and Pytorch when it comes to research purpose. __

It is nice and fancy when you listen to these terms and start writing code for your custom model to build something new for your application. You start writing the code and keep on writing to train a simple model and check its performance. In the end your model might not get to the stage where that can be deployed easily in the web due to constraints of memory and time, unless untill you are very skilled deep learning engineer. __

So nvidia guys have started build no code deep learning tool that helps to train a model for production without much expertise in deep learning. __

All you need to do is to:
- Get a proper data for your model
- Write a proper cfg file for training the model
- Write a proper cfg file for pruning the model
- Train the pruned model
- Infere the pruned model
- Deploy the model

I am sure you would know training and infering a model, purning was a new word for me while going through the docs. Unnecessary layers that are not needed are delete, basically the model is shrinked to lower size with out trading out the accuracy. This pruned model has to be trained for a few epochs so that the model performance can stay equal or close to unpruned model. Then the model is to be made deployment read and deployed in deepstream.



```
Note :  > Ever stuck on some error, please use nvidia forms rather stackoverflow or github issues. No one is gonna help you in stack so forget it when it come to nvidia tao. You will get reponse immediatley once you post a question in the form. At max they take a day to respond back to my knowledge.          
```




Happy learning.