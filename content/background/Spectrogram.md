---
title: Spectrogram
tags:
  - background
draft: false
date: 2024-02-10
---
A common way to visualise a sound recording is a **waveform**, which is simply a visualisation of the amplitude over time. This can give us a good idea of how loud audio is at different points in time, but it does not give us a good idea of whether the sound is high or low at any point in time. This is just what **spectrograms**  do: using what is called a *heatmap*, they **show the intensity of waves at different frequencies over time**. Frequencies are shown on the y-axis, while time is shown on the x-axis. This works very much like classical musical notation (whilst not being limited to certain discrete notes). More intense frequencies are commonly shown using brighter colours, while less intense frequencies are represented by more muted colours.

Spectrograms are very common in the field of [[Ecoacoustics]], as they allow researchers to get a quick overview of what is happening in long recordings.

![](https://www.researchgate.net/profile/Yoshiharu-Soeta/publication/286302352/figure/fig1/AS:304607751360512@1449635555451/Temporal-waveform-and-spectrogram-of-the-birdsong-stimuli-used-The-spectrogram-was.png)
> Waveform (left) and spectrogram (right) for a range of different birds. Source: [Soeta & Nakagawa 2015 Building & Environment](https://www.researchgate.net/publication/286302352_BEBirdMEG)

Spectrograms can be calculated using a method called [[Fast Fourier Transforms]], which can decompose a signal of mixed waves into its constituent parts.