# SCDFxIBM IOT101
![image](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/fire.png)

## Contents

1. [Short description](#short-description)
1. [Pitch video](#pitch-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Getting started](#getting-started)
1. [Built with](#built-with)
1. [Authors](#authors)
1. [License](#license)

## Short description

### What's the problem?

Punggol Digital District is identified to be the testbed for technology test cases, and realization of the Open Digital Platform (ODP). We aim to develop a usecase to demonstrate the how-to with the ODP. Our usecase consist of sensors integrated on ESP32, IBM Cloud, and AI at the edge. We aspire to use AI to detect anomalies in the communities such as fire hazard, rioting, loitering, such that the data can be fed to the system we have built on the IBM Cloud. SCDF personnel then is able to extract the necessary data points for resource planning.

### How can technology help?

IBM Cloud, sensors, ESP32, AI@Edge, are the necessary ingredients to help us as a nation to do more with less manpower. At the Command & Control Center, SCDF planner able to utilize the data to make decision, and strive towards optimal resource allocation. Prevention is better than cure, we hope the smart sensors installed is able to deter irresonsible and anti social behaviour.

### The idea

Our solution is a intergrated iot solution to act as preventive measure using machine learning/ai and using sensor on the cloud to alert the various users

## Pitch video

[![Watch the video]](https://www.youtube.com/watch?v=tFtTNHVMbq0)

## The architecture

![Video transcription/translation app](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/Architecture2.JPG)

1. Hazard is first detected by the Sipeed Module and sensors
2. The information is then send to an esp32 connected to the Sipeed Module
3. The esp32 will send the data to IBM Cloud
4. IBM Cloud

## Long description

[More detail is available here](DESCRIPTION.md)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system. 

###  Step 1
Machine code to GET key_gen Burn
  1. First download key_gen firmware and unzip it to key_gen_v1.2.bin
the Download AT at [The First key_gen Firmware](https://en.bbs.sipeed.com/uploads/default/original/1X/bca0832bed92a1ada63bd05327688784e2ef14d1.zip) and IT to the unzip at Thekey_gen_v1.2.bin

### Step 2
Use [kflash_gui](https://github.com/sipeed/kflash_gui/releases/tag/v1.5.3) burn key_gen_v1.2.bin

### Step 3
![image](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/step3.png)

### Step 4
Download face recognition model from Maixhub model platform
  1. Visit the [Maixhub model platform](https://www.maixhub.com/) homepage, register and log in.
  2.	Select [MaixPy Face Recognition Model]
(https://www.maixhub.com/index.php/index/index/detail/id/235) and click the download button.
  3. Click Submit to obtain recognition model
  
### Step 5
Burning face recognition model
  1. Use kflash_gui to flash the kfpkg model obtained in the previous step.
  2. After the burning is completed, the development board displays the MaixPy welcome interface.

### Step 6
Run MaixPy Face Recognition Script with MaixPy IDE
  1. Install the MaixPy IDE, see [MiaxPy IDE](https://blog.sipeed.com/p/612.html) for Details.
  2. Get face recognition script [demo_face_recognition.py](https://github.com/sipeed/MaixPy_scripts/blob/master/machine_vision/demo_face_recognition.py)
  3. Use MaixPy IDE to open the face recognition script, connect the development board, upload the script to the development board, you can see that face recognition has been successfully run on MaixPy. Users can modify our identification script to create more interesting applications.

## Built with

### Sipeed M1

Sipeed M1 is an open source AI development kit. It is useful in image recognition and any AI application. At the heart of the Sipeed M1 platform is the AI chip K210 by Kendryte, a dual-core RISC-V with an FPU. It serves as the core unit and dual-core processing with independent FPU, 64-bit CPU and 8M in-built SRAM. With a 400Mhz adjustable nominal frequency it supports multiplication, division and square root operation. The Sipeed M1 also integrates Micropython to make development pretty smooth and straightforward. With its edge computing capabilities, it can improve response time which is important when dealing with events such as arsoning, rioting, illegal gathering.

The Kendryte K210 is a system-on-chip (SoC) that integrates machine vision and machine hearing using TSMC’s ultra-low-power 28-nm advanced process with dual-core 64-bit processors for better power efficiency, stability and reliability. 

1.1   AI solution 

- 1.1.1 Machine Vision With machine vision capabilities, the Kendryte K210 can perform convolutional neural network calculations with low power consumption. It is capable of object detection, image classification and face recognition.

- 1.1.2 Machine Hearing The Kendryte K210 has machine hearing capabilities. The chip comes with a high performance microphone array audio processor for real-time source orientation and beamforming. 

- 1.1.3 Hybrid Audio/Vision Solution The Kendryte K210 combines machine vision and machine hearing to provide even more powerful features. In the application, both the sound source localization and the sound field imaging can be used to assist the machine vision to track the target. This allows us to detect the person's orientation.

### ESP32

The reason why we use [Esp32](https://techexplorations.com/guides/esp32/begin/esp32ard/#:~:text=The%20additional%20features%20that%20the,that%20alone%20is%20very%20desirable.&text=The%20ESP32%20dev%20kit%20is,board%20for%20a%20lower%20price.) is because it is better than Arduino. Esp32 not only can be used as an Arduino, it also provides Wireless Connectivity such as Wi-Fi and Bluetooth which most of the Arduino board does not provide. Micropython is used in conjunction with the board.

### DHTT Sensor
We will be using DHTT sensor to detect for the humidity and the Sipeed to detect for humans. If the detection of human is in a certain amount, it will be alerted to SPDF and the SPDF will check if there’s a riot going on. It works the same for the fire detection. Once detected fire, the data collected from the sensor and Sipeed will be sent to the IBM Cloud via Esp32. The data will then be send to the user which in our case, it is the SCDF people using IBM Bluemix push notification app. , alerting them about the scenarios so that they can prepare in advance.

### Node Red

Node red is a programming tool for wiring together hardware devices, APIs and online services in new and interesting ways. It provides a browser-based editor that makes it easy to wire together flows using the wide range of nodes in the palette that can be deployed to its runtime in a single-click.
Primarily, it is a visual tool designed for the Internet of Things, but it can also be used for other applications to very quickly assemble flows of various services
Browser Base Flow Editing
![Browser Base Flow Editing](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/flow.jpg)

### IBM Watson
We use IBM Watson to connect the esp 32 to cloud and then to send data. The reason why we use IBM Watson is because these platforms are more secure and offer many useful services, from getting data to analyse it using Machine learning algorithms. 

### Additional devices
As this is a prove of concept, many more IOT devices can be connected to allow us to track more data and thus send more vital data to the authoritives. 

## Authors

* **Ashwin Dinesh**  
* **Lim Zi Xiong**  
* **Rusyaidi Bin Abdul Rashid**  
* **Chew Liang Zhi**  

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details



