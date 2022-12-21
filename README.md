
**Image synthesis** is one of the computer vision fields with the most spectacular recent development, but also among those with the greatest computational demands.

Recently,**diffusion models**, which are built from a hierarchy of denoising autoencoders, have shown to achieve impressive results in image synthesis and beyond and define the state-of-the-art in class-conditional image synthesi and super-resolution.

Diffusion Models are probabilistic models designed to learn a data distribution p(x) by gradually **denoising** a normally distributed variable, which corresponds to learning the reverse process of a fixed Markov Chain of length T.

<p align="center">
  <img src="assets/modelfigure.png">
</p>

Images(x) are going through the diffusion process to add noise sequentially, Then the U-net architecture is used to denoise the image step by step. **Latent Diffusion Models (LDMs)** consist of an encoder and decoder to not feed the input image directly to diffusion process. Using autoencoder to first encode images to latent space and then going through diffusion process in laten spaces. These low resolution images can be decoded to get back to the predicted image.


**Contrastive Language-Image Pre-Training (CLIP)** is a neural network trained on a large set (400M) of image and text pairs. As a consequence of this multi-modality training, CLIP can be used to find the text snippet that best represents a given image, or the most suitable image given a text query.

The following steps are used in application of LDMs:
  1. Load the autoencoder model which will be used to decode the latents into image space.
     **diffusers.AutoencoderKL.from_pretrained()**
  2. Load the tokenizer and text encoder to tokenize and encode the text. Tokenizer is a common task in NLP, seperating a piece of text into small unit called      tokens.Byte Pair Encoding (BPE) is a widely used tokenization method among transformer-based models.
     **transforms.CLIPTokenizer.from_pretrained**


***Reference:***
https://arxiv.org/abs/2112.10752
https://towardsdatascience.com/linking-images-and-text-with-openai-clip-abb4bdf5dbd2

