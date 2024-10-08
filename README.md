# Image_Colorization using pix2pix

This project implements an image colorization technique using the Pix2Pix GAN (Generative Adversarial Network) framework. The model takes grayscale images as input and generates corresponding color images. It leverages the Pix2Pix architecture to learn the mapping from grayscale to color images effectively.

## Dataset 
The Dataset used in the pix2pix model is [dataset](https://www.kaggle.com/datasets/shravankumar9892/image-colorization).
This dataset contains two folder one is **l** -> contains **grayscale image** and **ab** -> **contains a and b dimensions of LAB**

## Why pix2pix?
Pix2Pix was introduced in the paper "**Image-to-Image Translation with Conditional Adversarial Networks**" by Isola et al. (2017). The model uses a generator and discriminator to achieve image-to-image translation tasks. Here’s why Pix2Pix is particularly well-suited for image colorization:

    **Conditional Learning:** Pix2Pix allows for conditional generation based on input images, making it ideal for colorization where the output is directly dependent on the grayscale input.

   ** Adversarial Training:** The generator and discriminator work against each other, improving the realism of the generated images. The discriminator helps the generator create more convincing outputs by providing feedback during training.

    **Versatility:**  The architecture can be easily adapted for various image-to-image translation tasks beyond colorization, making it a powerful tool in computer vision.

## A small summary about U-Net Architecture
The generator in this project is based on the U-Net architecture, which was originally designed for biomedical image segmentation. It has since been widely adopted in various image-to-image translation tasks, including colorization. Key features of the U-Net architecture include:

    **Encoder-Decoder Structure:** U-Net has a symmetric encoder-decoder structure that captures context through downsampling (encoder) and allows precise localization via upsampling (decoder).

    **Skip Connections:** The architecture includes skip connections between corresponding encoder and decoder layers. This helps preserve spatial information, which is crucial for generating high-quality images.

    **Effective Learning:** U-Net's architecture enables efficient learning from fewer training images, making it effective for tasks with limited datasets.
