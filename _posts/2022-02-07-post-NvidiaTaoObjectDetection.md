---
title: "Nvidia Tao for Object Detection"
date: 2022-07-02T15:34:30-04:00
categories:
  - blog
tags:
  - Computer Vision 
---


# Nvidia Tao Tutorial


# Installing Docker 

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


My system specs:

```python
(base) saiteja@detecttechvm03:~/DetectTechWork$ nvidia-smi
Sat Jul  2 17:13:57 2022
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 510.47.03    Driver Version: 510.47.03    CUDA Version: 11.6     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA A100-PCI...  On   | 00000000:06:00.0 Off |                    0 |
| N/A   49C    P0    59W / 250W |      0MiB / 40960MiB |      0%      Default |
|                               |                      |             Disabled |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|  No running processes found                                                 |
+-----------------------------------------------------------------------------+
```






# Dataset Preparation

I am using VisDrone dataset.(https://github.com/VisDrone/VisDrone-Dataset)
The script below downloads necessary files.


```python
import gdown
url = 'https://drive.google.com/uc?id=1a2oHjcEcwXP8oUF95qiwrqzACb2YlUhn'
output = 'train.zip'
gdown.download(url, output, quiet=False)

url = 'https://drive.google.com/uc?id=1bxK5zgLn0_L8x276eKkuYA_FzwCIjb59'
output = 'val.zip'
gdown.download(url, output, quiet=False)

url = 'https://drive.google.com/uc?id=1PFdW_VFSCfZ_sTSZAGjQdifF_Xd5mf0V'
output = 'test.zip'
gdown.download(url, output, quiet=False)
```







