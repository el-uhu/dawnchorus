---
title: Physics lab on developing specifications
tags:
  - teaching
draft: false
date: 2024-02-13
---


> [!info] Setting and Aim
> Present student with real-life problems (semi-structured) that involve some level of research and need to be tackled practically as well as theoretically.
> 
> **Aim:**
> - Develop specifications for [[Dawn Chorus ARU]]
> - Develop specifications for [[Sound Showers]]

## Group 1 - Characterisation of Power Consumption
![[E06C2E8A-FE96-4065-A79F-322F42E59E91_1_102_a.jpeg]]
### List of provided items
- 1 [Raspberry Pi Zero 2 W](https://www.raspberrypi.com/products/raspberry-pi-zero-2-w/) with [Witty Pi 3 Mini](https://www.uugear.com/product/witty-pi-3-mini-realtime-clock-and-power-management-for-raspberry-pi/)and [Pirate Audio Dual Mic](https://shop.pimoroni.com/products/pirate-audio-dual-mic?variant=32236592693331) attached
	- running the [cliprecorder.py](https://github.com/pimoroni/pirate-audio/blob/master/clip-recorder/cliprecord.py) script
- 1 [USB Power Meter](https://m.media-amazon.com/images/I/C1krxbAquzL.pdf)
- 1 USB Charger
- 1 USB-A to micro-USB cable

### Tasks
- Characterise the power consumption of the raspberry pi zero with Witty Pi and Pirate Audio Dual Mic shield while recording and while idle
	- Familiarise yourself with the available equipment
		- What does the Power Meter do and how does it work?
		- Which is the correct USB port to use to power the Raspberry Pi?
		- What is the role of the Witty Pi shield?
		- What is the role of the Pirate Audio Dual Mic shield?
		- What does the software running on the Raspberry Pi do?
	- Connect the USB power supply to the USB Power Meter (IN Port)
	- Reset the Power Meter if necessary
	- Plug the Raspberry Pi into the USB Power Meter (Out Port)
	- Set the Raspberry Pi to "Record"
	- Measure the power consumption
	- Reset the Power Meter and repeat the procedure in Idle Mode
	- Calculate the power consumption per hour for the two modes (idle, recording).
	- Assuming a battery capacity of 10000mAh, calculate how many days the power would last if the unit were to record twice a day for two hours and were idle for the remaining time
	- What would be the battery capacity necessary to keep recording for three days?
	- Suggest modifications that could reduce power consumption of the unit.

## Group 2 - Characterisation of Battery Pack and Solar Panel
![[18A2AE78-25EC-4124-A939-9E0595A33D1C_1_102_a.jpeg]]
### List of provided items
- 1 [Waveshare Solar Manager Unit (C)](https://www.waveshare.com/Solar-Power-Manager-C.htm)
	- 3x 18650 batteries (3000mAh each) installed
- [1 Outdoor Wireless Camera Solar Panel](https://www.amazon.de/dp/B0B9XM8M65?psc=1&ref=ppx_yo2ov_dt_b_product_details)
	- 1 USB-C adapter provided
- 1 [USB Power Meter](https://m.media-amazon.com/images/I/C1krxbAquzL.pdf)
- 1 USB-C to USB-C power cable

### Tasks
- Characterise the solar panel and battery pack assembly
	- Familiarise yourself with the available equipment
		- Solar Manager Unit
			- What does the solar manager do?
			- What is meant by MPPT and why is it necessary when charging a battery using photovoltaic modules?
			- Based on the selected parts, what is the theoretical capacity of the unit?
			- Assuming average power draws of 5mAh, 50mAh and 500mAh, how long would a fully charged battery last?
			- Where does the Raspberry Pi fall? (compare with Group 1)
		- Solar Panel
			- What are the electrical characteristics (wattage, voltage) of the solar panel?
			- What would be the expected power output over the course of a day?
			- Assuming a fully charged battery pack, and the most accurate estimate of the average power draw of the Raspberry Pi over a day, would you expect the combination of solar panel and battery to reliably power the raspberry pi long term?
	- Devise a test to measure the power output of the solar panel under real world conditions.
		- What are the factors that affect the power output?
		- What would be an optimal position and orientation of the solar panel?
		- Set up the solar panel and connect it to the Solar Manager Unit via the Power meter using the USB-C connections. 
			- Measure the power output under different lighting conditions.
	- Formulate simple instructions on how to position and orientate the solar panel based on your findings.

## Group 3 - Characterisation of the [[Sound Showers]]
### List of items provided
- 2 parabolic reflector umbrellas
- Measuring tape
- Soundfiles
	- Sinus tones of different frequencies
	- Nature recordings
- 2 small speakers
- USB-C to 3.5mm Jack (female) adapter
- Lightning to 3.5mm Jack (female) adapter

### Tasks
- What even is a sound shower?
- The umbrella is parabolic, measure the umbrella and try to work out a good estimate for the parameters describing the parabola
- For optimal sound reflection by the umbrella the speaker pointing into it needs to be positioned in the focus of the parabola. How far away from the tip is the focus of this particular parabola located?
- Use the provided speaker, your phone and the provided audio files to test for optimal positioning of the speaker.
	- How do the frequencies of the sound samples relate to the quality of reflection by the umbrella?
- Suggest how the umbrella can be improved to become a better reflector.