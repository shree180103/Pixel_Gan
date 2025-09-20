# Pix2Pix_Gan
Pix2Pix GAN is a conditional Generative Adversarial Network (cGAN) designed for image-to-image translation tasks. Unlike standard GANs (which generate images from random noise), Pix2Pix generates images conditioned on an input image.

![](https://github.com/shree180103/Pixel_Gan/blob/main/imgs/Screenshot%202025-09-20%20232123.png)

# Model architecture
![](https://github.com/shree180103/Pixel_Gan/blob/main/imgs/image.png)

Generator: The U-Net is a type of encoder-decoder network with skip connections. It was originally introduced for segmentation tasks, where keeping both high-level/contextual features and low-level/spatial detail is essential. Pix2Pix adopts this architecture for its generator.

Discriminator:The discriminator in Pix2Pix is implemented as a PatchGAN. The key idea is: instead of classifying the entire image as real or fake, the discriminator works on local image patches (e.g. 70×70 patches) and produces a feature map of decisions (one per patch).

# Loss Functions

<img width="1228" height="114" alt="image" src="https://github.com/user-attachments/assets/5942a186-13ed-4380-94cc-ead5d6a2ab1b" />

<img width="678" height="172" alt="image" src="https://github.com/user-attachments/assets/23198d90-0f3f-4656-b85a-6d763896b9ce" />

<img width="779" height="153" alt="image" src="https://github.com/user-attachments/assets/e8405860-b632-4807-b777-5ffc551ed489" />

We use this Lagrangian to force the effect of the L1 norm without overpowering the GAN loss. 

# Results

![scdqcq](./output_satalite%20images.png)

![](https://github.com/shree180103/Pixel_Gan/blob/main/output.png)

