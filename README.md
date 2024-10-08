# Image_Colorization using pix2pix

This project implements an image colorization technique using the Pix2Pix GAN (Generative Adversarial Network) framework. The model takes grayscale images as input and generates corresponding color images. It leverages the Pix2Pix architecture to learn the mapping from grayscale to color images effectively.

## What is GAN?

Generative Adversarial Networks (GANs) are a class of machine learning frameworks introduced by Ian Goodfellow et al. in 2014. GANs are designed for unsupervised learning and are particularly effective in generating new data samples that resemble a given training dataset. The key components of a GAN are:

  **Generator:** This component generates new data samples from random noise. Its goal is to create data that is indistinguishable from real data. The generator learns to map input noise to the data distribution of the target domain.

  **Discriminator:** The discriminator acts as a critic that evaluates the authenticity of the generated data. It receives both real data and fake data produced by the generator, and its task is to classify them correctly as real or fake.

   **Adversarial Training:** The generator and discriminator are trained simultaneously in a competitive setting. The generator aims to improve its ability to produce realistic samples to fool the discriminator, while the discriminator strives to improve its accuracy in distinguishing real from fake data. This adversarial process leads to the generator producing increasingly realistic samples over time.

## Dataset 
The Dataset used in the pix2pix model is [dataset](https://www.kaggle.com/datasets/shravankumar9892/image-colorization).
This dataset contains two folder one is **l** -> contains **grayscale image** and **ab** -> **contains a and b dimensions of LAB**

## Why pix2pix?
Pix2Pix was introduced in the paper "**Image-to-Image Translation with Conditional Adversarial Networks**" by Isola et al. (2017). The model uses a generator and discriminator to achieve image-to-image translation tasks. Here’s why Pix2Pix is particularly well-suited for image colorization:

 **Conditional Learning:** Pix2Pix allows for conditional generation based on input images, making it ideal for colorization where the output is directly dependent on the grayscale input.

 **Adversarial Training:** The generator and discriminator work against each other, improving the realism of the generated images. The discriminator helps the generator create more convincing outputs by providing feedback during training.

 **Versatility:**  The architecture can be easily adapted for various image-to-image translation tasks beyond colorization, making it a powerful tool in computer vision.

 **Research paper based on pix2pix:**\
 ->[For understanding the pix2pix gan and this paper prodives optimization also](https://arxiv.org/pdf/1611.07004)\
 ->[This paper for DCGAN and basic idea of gan](https://arxiv.org/abs/1511.06434)

## A small summary about U-Net Architecture
The generator in this project is based on the U-Net architecture, which was originally designed for biomedical image segmentation. It has since been widely adopted in various image-to-image translation tasks, including colorization. Key features of the U-Net architecture include:

  **Encoder-Decoder Structure:** U-Net has a symmetric encoder-decoder structure that captures context through downsampling (encoder) and allows precise localization via upsampling (decoder).

   **Skip Connections:** The architecture includes skip connections between corresponding encoder and decoder layers. This helps preserve spatial information, which is crucial for generating high-quality images.

   **Effective Learning:** U-Net's architecture enables efficient learning from fewer training images, making it effective for tasks with limited datasets.

   ->This website gives theortical understanding and code for u-net arhcitecture [here](https://paperswithcode.com/method/u-net)

## Reference
Pytroch -> https://www.learnpytorch.io/
DCGAN in Pyroch -> https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html
Threotical video for understanding the GAN -> https://youtu.be/Gib_kiXgnvA?si=JbnLad4BbqKIhfpe

