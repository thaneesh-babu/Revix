## Generative models in the past

There are two ways of approaching the task of generating music: symbolic and non-symbolic. The symbolic approach easens the modeling process as we would be working in lower-dimensional space albeit with the tradeoff of being limited to a sequence of notes and/or using only a small number of instruments. The non-symbolic approach hopes to generate music as raw audio, which turns out to be more challenging, as that would entail working with loads of data.

## Jukebox

This model uses deep generative models to produce music in the raw audio space, using a hierarchial VQ-VAE architecture with a loss function aimed at retaining as much musical information as possible with high levels of compression at the same time.

## Making sense of music encoding

Music in the raw audio space can be represented as a continuous waveform x ∈ [−1, 1]<sup>T</sup>, where T = audio duration \* sampling rate (∈ [16 kHz, 48 kHz]). Hence, learning a generative model for music is computationally intensive, as the input vector would be insanely long for a multi-minute snippet.

## Autoencoders (AE)

These encoders, in short, convert information (images/videos/audio and the like, which would be an input vector of significantly high dimension) to a lower dimension space through a latent vector and decode it back to the original dimension. The goal is to minimize the loss as much as possible, usually used with the MSE loss.

## Variation Autoencoders (VAE)

These overcome the limitations of AEs by regularizing the latent space to make it more continous and generative more meaningful samples. This entails forming the mean vector and standard deviation vector from the input vector and sampling from it to the decoder.
