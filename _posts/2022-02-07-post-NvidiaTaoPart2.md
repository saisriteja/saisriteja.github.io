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

I am using the mask detection dataset from [kaggle](https://www.kaggle.com/datasets/prithwirajmitra/covid-face-mask-detection-dataset). My moto is to detect the if the person is wearing mask or not. 


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

- a. Username: "$oauthtoken"
- b. Password: "YOUR_NGC_API_KEY"



