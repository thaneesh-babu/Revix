## Generative models in the past

There are two ways of approaching the task of generating music: symbolic and non-symbolic. The symbolic approach easens the modeling process as we would be working in lower-dimensional space albeit with the tradeoff of being limited to a sequence of notes and/or using only a small number of instruments. The non-symbolic approach hopes to generative music as raw audio, which turns out to be more challenging, as that would entail working with loads of data.

## Jukebox

This model uses deep generative models to produce music in the raw audio space, su

## Autoencoders

These encoders, in short, convert information (images/videos/audio and the like) to a lower dimension space through a latent vector and decode it back to the original dimension. The goal is to minimize the loss as much as possible, usually used with the MSE loss

## Variation Autoencoders (VAE)

These overcome the limitations of AEs by regularizing the latent space to make it more continous and generative more meaningful samples.
