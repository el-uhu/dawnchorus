---
title: Autonomous Recording Units
tags:
  - recording
draft: false
date: 2024-02-13
aliases:
  - ARU
  - ARUs
  - Autonomous Recording Unit
authors:
  - Lukas Hutter
---


When studying the sound of a landscape, a common challenge that arises is audio-recording itself. *How do we record audio over long timespans in remote locations, far away from the next power supply?*

# The Challenge
Of course, people studying ecoacoustics can build a portable recording rig (an audio recorder, some spare batteries and some really nice [[Microphones|microphones]], should do) pack a thermos and some sandwiches and venture out into the field to record sounds of the wild in high definition. Lots of people conduct work in the field that way and we can thank them for some breathtaking and heart-wrenching recordings. The problem is that this approach doesn't scale particularly well. 

# The Solution
To address this issue, people have developed **Autonomous Recording Units (ARUs)** that fit into a waterproof box, are equipped with hefty batteries and can be programmed to record audio at set times or whenever a continuously running algorithm detects a particular sound.

## The Problem of Cost

![BAR-LT](https://static.wixstatic.com/media/e25630_95f4e23b18604db7a9c3ceb6a0564f8a~mv2.jpg/v1/fill/w_1040,h_779,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/e25630_95f4e23b18604db7a9c3ceb6a0564f8a~mv2.jpg)
> The BAR-LT ARU by FrontierLabs (*Image: FrontierLabs*)

Professional grade ARUs easily cost a couple of hundred euros. Good examples of commonly used ones are the units designed by [FrontierLabs](https://www.frontierlabs.com.au), which are equipped with high-grade, sensitive and low noise audio components, pack in loads of storage and battery life or even optional solar panels. However, their power is reflected in the pricepoint - the base unit costs 800€.

Even monitoring a handful of locations using a device is impossible for many projects that run on very limited budgets.

# AudioMoth
![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5f7b7f5dc9e77c001621490b/images/611ea390b55c2b04bf6e00e8/file-HlPpx242ll.png)
> The AudioMoth (*Image: Rainforest Connection*)

In 2017, an interdisciplinary collaboration project between the University of Oxford and the University of Southampton led by computer scientist Alex Rogers tried to tackle this problem and developed an [audio recorder that's integrated into a single printed circuit board (PCB) board](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.12955) called [AudioMoth](https://www.openacousticdevices.info/audiomoth), which can be powered by three AA batteries and costs (depending on circumstance [^1]) between 50€ and 130€.

## Trade-offs
Of course a unit that cheap is not without tradeoffs. Whereas higher-priced units use high quality omnidirectional microphones, the AudioMoth uses a [[MEMS]]-type [[Microphones|microphones]] (a miniaturised microphone that can be integrated onto PCB, similar to the ones used in your phone). Compared to higher grade microphones, MEMS-type microphones are more mechanically and electrically robust, can be more easily integrated into electrically noisy environments and are relatively cheap. However, they also have a wider range of directionality, higher output signal (thus requiring less amplification), overall lower noise and higher sensitivity. Yet, arguably, perhaps lower audio quality may not be the be all end all in ecoacoustic studies, particularly when scale matters and sufficient information can be extracted from lower quality recordings.

# DIY ARUs

![SOLO](https://besjournals.onlinelibrary.wiley.com/cms/asset/629da62c-dbed-4961-97b9-10db6131c16f/mee312678-fig-0001-m.jpg)
> The Raspberry Pi-based ARU "SOLO" (Image: Whytock & Christie, 2017[^2])

In a similar attempt at reducing the costs for ARUs, several projects have developed ARUs from off-the-shelf components such as Raspberry Pis and USB soundcards [^2], [^4]. They commonly employ car batteries, or hefty powebanks and expose a lavalier microphone to the elements. 

%%# Comparison
A team of researchers have characterised the performance of AudioMoth in depth[^3], while no such systematic characterisation could be found for BAR-LT, hence the table below reflects data listed on the company website.

|  | AudioMoth | BAR-LT | SOLO |
| ---- | ---- | ---- | ---- |
| Energy consumption |  |  |  |
| Cost | 130€ | 800€ |  |
| Battery capacity | 9000mAh |  |  |
| SNR (Signal-to-Noise Ratio) |  |  |  |
| Frequency Range |  |  |  |
| Sampling rate | 384 kHz |  |  |
| Bit depth |  |  |  |
| Supported storage |  |  |  |
| GPS capability | via add-on |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

> [!info] Sound Quality Terms Explained
> Check out the article on [[Digital Audio and the wav-Format]] for an explanation of [[Digital Audio and the wav-Format#Sampling Rate|sampling rate]] and [[Digital Audio and the wav-Format#Bit Depth|bit depth]]


%%


> [!hint] Active Development
> We've decided to have a shot at developing our own solar-powered, RPi Zero-based ARU, read more on it [[Dawn Chorus ARU|here]].

[^1]: The units sell for 130€ at veldshop.nl and other specialist online shops, but [group-buy options](https://groupgets.com/manufacturers/open-acoustic-devices/products/audiomoth) exist for larger number that significantly reduce the per unit cost.

[^2]: [Whytock, R.C. and Christie, J. (2017), Solo: an open source, customizable and inexpensive audio recorder for bioacoustic research. Methods Ecol Evol, 8: 308-312.](https://besjournals.onlinelibrary.wiley.com/doi/10.1111/2041-210X.12678)

[^3]: [Lapp S, Stahlman N, Kitzes J. A Quantitative Evaluation of the Performance of the Low-Cost AudioMoth Acoustic Recording Unit. Sensors (Basel). 2023](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10256106/pdf/sensors-23-05254.pdf)

[^4]: Kim Hendrikse: [stbs-aru on GitHub](https://github.com/hcfman/sbts-aru?tab=readme-ov-file)