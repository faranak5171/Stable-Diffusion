
**Image synthesis** is one of the computer vision fields with the most spectacular recent development, but also among those with the greatest computational demands.

Recently,**diffusion models**, which are built from a hierarchy of denoising autoencoders, have shown to achieve impressive results in image synthesis and beyond and define the state-of-the-art in class-conditional image synthesi and super-resolution.

Diffusion Models are probabilistic models designed to learn a data distribution p(x) by gradually **denoising** a normally distributed variable, which corresponds to learning the reverse process of a fixed Markov Chain of length T.

<p align="center">
  <img src="assets/modelfigure.png">
</p>

Images(x) are going through the diffusion process to add noise sequentially, Then the U-net architecture is used to denoise the image step by step. **Latent Diffusion Models (LDMs)** consist of an encoder and decoder to not feed the input image directly to diffusion process. Using autoencoder to first encode images to latent space and then going through diffusion process in laten spaces. These low resolution images can be decoded to get back to the predicted image.


Reference: https://arxiv.org/abs/2112.10752
