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



You could have listen to pytorch or tensorflow when you enter in the world of Machine Learning. These are the two important frameworks that are currently the best for implementation any deep learning model.

One would prefer tensorflow when it comes to deployment and Pytorch when it comes to research purpose.

It is nice and fancy when you listen to these terms and start writing code for your custom model to build something new for your application. You start writing the code and keep on writing to train a simple model and check its performance. In the end your model might not get to the stage where that can be deployed easily in the web due to constraints of memory and time, unless untill you are very skilled deep learning engineer.

So nvidia guys have started build no code deep learning tool that helps to train a model for production without much expertise in deep learning.

All you need to do is to:
- Get a proper data for your model
- Write a proper cfg file for training the model
- Write a proper cfg file for pruning the model
- Train the pruned model
- Infere the pruned model
- Deploy the model

I am sure you would know training and infering a model, purning was a new word for me while going through the docs. Unnecessary layers that are not needed are delete, basically the model is shrinked to lower size with out trading out the accuracy. This pruned model has to be trained for a few epochs so that the model performance can stay equal or close to unpruned model. Then the model is to be made deployment read and deployed in deepstream.



***
Note : Ever stuck on some error, please use nvidia forms rather stackoverflow or github issues. No one is gonna help you in stack so forget it when it come to nvidia tao. You will get reponse immediatley once you post a question in the form. At max they take a day to respond back to my knowledge.          
***



## Installation Process


It is always prefered to read the [offical document](https://docs.nvidia.com/tao/tao-toolkit/text/tao_toolkit_quick_start_guide.html) and procced for installtion process. I encourge you to do that, the given below are quick reference to crosscheck.

System Specs:

32 GB system RAM
32 GB of GPU RAM
8 core CPU
1 NVIDIA GPU
100 GB of SSD space


## Installing Docker 

```python
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

 sudo mkdir -p /etc/apt/keyrings
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

 echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

The below extra steps are to make sure the docker can be used without sudo access.

```
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker 
docker run hello-world
```



```
distribution=$(. /etc/os-release;echo $ID$VERSION_ID) \
      && curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
      && curl -s -L https://nvidia.github.io/libnvidia-container/$distribution/libnvidia-container.list | \
            sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
            sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list


sudo apt-get install -y nvidia-docker2
sudo systemctl restart docker
sudo docker run --rm --gpus all nvidia/cuda:11.0.3-base-ubuntu20.04 nvidia-smi

```




## Get an NGC Key

```
Get an NGC account and API key:
- Go to NGC and click the TAO Toolkit container in the Catalog tab. This message is displayed: “Sign in to access the PULL feature of this repository”.
- Enter your Email address and click Next, or click Create an Account.
- Choose your organization when prompted for Organization/Team.
- Click Sign In.
```

## Login NGC docker

Log in to the NGC docker registry (nvcr.io) using the command docker login nvcr.io and enter the following credentials:

```
- a. Username: "$oauthtoken"
- b. Password: "YOUR_NGC_API_KEY"
```





Happy learning.