---
layout: post
title: Building Better Deep Learning Models
description:
date: 2025-01-22 16:40:16
tags: DeepLearning
image: img/postbanners/2024-08-07-convert-datetime2-bigint.png
---

# Building Deep Learning Models


In my previous blog, I discuss the AutoDL pipeline, which you can explore here: [AutoDL Blog](https://saisriteja.github.io/2025/01/22/AutoDL.html). The final module of this pipeline focuses on model dependability—helping us understand when a model performs well and when it fails. One key insight is that no matter how much you manipulate or augment poor-quality data, it will not improve the model's output. Therefore, it's crucial to break free from this cycle and identify where the issue lies if the model's accuracy plateaus.

Deep learning models are inherently probabilistic and heavily dependent on the data they are trained on. This makes them particularly vulnerable to out-of-distribution data, posing a significant challenge both for the model and for human interpretation.

To overcome these challenges, improving the priors and representations within the model is essential. For instance, in self-driving cars, while RGB cameras may struggle in low-light conditions, thermal cameras can provide valuable insights by detecting heat signatures.

Advancements in model architectures and algorithms can help push the boundaries of performance, enabling more robust handling of edge cases and out-of-distribution scenarios. Incorporating multimodal inputs, such as text, speech, or novel sensors (e.g., thermal cameras), can further enhance model robustness by providing better priors and improving the model's ability to handle complex, real-world applications.


<div align="center">
    <a href="https://drive.google.com/file/d/1oaHXFoyBH1w4nQNuxQ1sIVaPlcgpc-yC/view?usp=sharing">
        <img src="https://drive.google.com/thumbnail?id=1oaHXFoyBH1w4nQNuxQ1sIVaPlcgpc-yC&sz=w1000" alt="Model Explainability" style="max-width: 100%; height: auto;">
    </a>
</div>



# Overview of Key Technologies



## MultiModal Stack

In this approach, new modalities are integrated alongside existing ones, such as text, speech, or advanced cameras, to enhance model performance. The goal is to leverage complementary information from different modalities—information that may not be present in the current modality but exists in another. The model then selects the most relevant information from both sources to make a more informed decision.


## Model Explainability

<div align="center">
    <a href="https://drive.google.com/file/d/1w7NDzXJEU7WaM7bIlK8AIMv7365WeY6U/view?usp=sharing">
        <img src="https://drive.google.com/thumbnail?id=1w7NDzXJEU7WaM7bIlK8AIMv7365WeY6U&sz=w1000" alt="Model Explainability" style="max-width: 100%; height: auto;">
    </a>
    <p style="text-align: center;">On the left, the person is not visible in the low-light RGB image, but is clearly seen in the thermal image. On the right, the SPAD camera captures high-resolution output without read noise due to its hardware, offering enhanced visibility even in low-light conditions, such as at night.</p>
</div>



### Computer Vision Stack

1. **Lensless Imaging**  
   Lensless imaging leverages computational methods to reconstruct images without traditional optical lenses. It captures light patterns using a sensor array and processes the data using algorithms to generate high-quality 3D images.

2. **Thermal Cameras**  
   Thermal cameras detect infrared radiation emitted by objects, converting it into visible images. These cameras are especially useful in low-light conditions and for detecting temperature anomalies, commonly used in medical imaging, surveillance, and night vision.

3. **SPAD Cameras (Single-Photon Avalanche Diode)**  
   SPAD cameras are highly sensitive sensors that detect single photons, enabling ultra-low light imaging. They are used in applications such as time-of-flight (ToF) imaging, LiDAR systems, and quantum optics, providing high-resolution depth information.

4. **Depth Cameras (LiDAR)**  
   LiDAR uses laser pulses to measure distances, creating precise 3D maps of environments. It is a key technology in autonomous vehicles, robotics, and any application requiring accurate depth sensing, providing detailed environmental awareness.




## Algorithm Stack
### Generative AI

1. **GANs (Generative Adversarial Networks)**  
   GANs consist of two networks—a generator and a discriminator—that work in opposition. The generator creates data, while the discriminator evaluates it. This adversarial process improves the quality of generated content over time, commonly used for image synthesis and enhancement tasks.

2. **Diffusion Models**  
   Diffusion models generate data by progressively denoising random noise, reversing a process of gradual degradation. They are known for their ability to create high-quality, diverse images and are applied to tasks like image synthesis and inpainting.

3. **Flow-Based Models**  
   Flow-based models transform a simple distribution (e.g., Gaussian noise) into a complex distribution by learning invertible transformations. They are particularly suited for tasks requiring exact likelihood computation, such as density estimation and image generation.

4. **NeRFs (Neural Radiance Fields)**  
   NeRFs model 3D scenes by representing the interaction of light within the scene, enabling the generation of highly realistic 3D views from 2D images. They are commonly used in virtual reality, 3D rendering, and photorealistic scene generation.

5. **Gaussian Splatting**  
   Gaussian splatting involves representing 3D scenes or objects using points with associated Gaussian distributions. This technique provides an efficient and accurate way to synthesize 3D objects, enhancing volumetric rendering quality.


### Image Restoration/Cleaning

1. **U-Net Architectures**  
   U-Net-based architectures are widely used for image restoration and segmentation. They excel in capturing fine spatial details and contextual information. Notable U-Net variants include:
   - **Restormer**: Optimized for image denoising and deblurring tasks, providing enhanced restoration quality.
   - **UFormer**: Combines U-Net with transformers to improve feature extraction and restoration accuracy, especially for high-quality image reconstruction.
   - **AutoDir**: An autoencoder-based U-Net variant designed to perform image restoration in an unsupervised manner.





## Slides

- [Diffusion Slides](https://docs.google.com/presentation/d/1yYPugrsdYUut1hcbN96eXrzerQguvg2CTnJaPIk_lug/edit?usp=sharing)
- [Gaussian Splatting Slides](https://docs.google.com/presentation/d/1OKtE_RMAl_JY3t2DGcpUf0cb-tvRH6W0YzRLrIj501w/edit?usp=sharing)
