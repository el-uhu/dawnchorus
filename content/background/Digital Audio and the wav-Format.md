---
title: Digital Audio and the wav-Format
tags:
  - "#background"
draft: false
date: 2024-02-10
---


![](https://routenote.com/blog/wp-content/uploads/2022/08/What-is-bit-depth-in-digital-audio-RouteNote-Blog-1-2.jpg)
> Source: [RouteNote](https://routenote.com/blog/what-is-bit-depth/)

# Sound
Soundwaves are fluctuations of the pressure of a medium, such as air. The height of this fluctuation is called **amplitude** and corresponds to the **loudness** of a sound (measured in decibel, $dB$). 
The number of full up-and-down movements of pressure in a unit of time is called its **frequency**, which we perceive as the **pitch** (measured in $Hz$), i.e. how high or low a sound is. 
Using microphones pressure fluctuations in, say, air can be turned into an electrical signal, which correspond to *continuous* fluctuations of voltage over time. 

# Analog vs. Digital Signals
When we want to turn these continuous *analog* signals into something that a computer can work with more easily we convert them into *digital* signals that can be represented as zeroes and ones. To do this, we need to slice up a continuous signal (think of a smooth wave) into little chunks and measure the amplitude (height of the wave). 

# Sampling Rate
The number of slices per unit time is called the **sampling rate** (expressed in $Hz$). The higher the sampling rate, the more slices per unit time, and the closer the resemblance of a digital approximation to the actual analog signal. 

# Bit Depth
The second key factor that affects the quality of resemblance between the digital representation and the analog signal is the **bit depth**, which is the number bits used to represent changes in amplitude. The higher the bit depth the more steps are used to mimic a smooth change in amplitude.

# A Useful Analogy
In short, this analogy might help: **Imagine you're painting a picture, but you're only given a set number of colours and are only allowed to use a defined number of strokes. The selection of colours corresponds to the bit depth, while the number of strokes corresponds to the sampling rate**

# The `.wav` - Format
Having turned an analog signal into a digital one using appropriate sampling rate and bit depth, we have what we could call  digital audio, which is commonly stored using the `.wav` format (pronounced *wave*). This is a binary format, meaning that if you were to open the file in a text editor, you would find little that you would recognise, but computers can work with binary formats very efficiently. As opposed to `.mp3`, `.wav` is **uncompressed**, meaning we didn't use any mathematical tricks to reduce the file size. 

# Problems with Compression
When analysing audio, working with uncompressed audio is very important, as compression can lead to artefacts - the appearance of effects that result only from our manipulation of the data (e.g. the compression) and aren't really present in the raw data.