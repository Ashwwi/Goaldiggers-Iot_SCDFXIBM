# SCDFxIBM IOT101
![image](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/fire.png)

## Contents

1. [Short description](#short-description)
1. [Pitch video](#pitch-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Getting started](#getting-started)
1. [Running the tests](#running-the-tests)
1. [Built with](#built-with)
1. [Authors](#authors)
1. [License](#license)
1. [Acknowledgments](#acknowledgments)

## Short description

### What's the problem?

Punggol Digital District is powered by high technology such as the use of Open Digital Platform that integrates various smart city solutions together. Hence the cost of creating such places is high, thus if there's any chaos such as fire outbreaks/ riots, the cost of repairment will be high too. As such, fire/riot detection is important to keep the cost low and keep the neighbourhood safe.

Fire/riot detection also allows the SCDF officers more time to prepare and equip themselves with the proper gear. This allows them to be better suited at undertaking the task at hand. Furthermore, faster reactions can be vital in minimizing damage done by fires or riots.

### How can technology help?

Technologies are able to play a big part in fire detection. Machines are faster than the average human reaction thus utilizing that speed can be beneficial in detecting fires. Our group decided to equip devices capable of detecting fires at many locations. The sipeed m1 module is used as our device as it was compact, easy to install and was able to achieve our goals.

### The idea

Detection is key in eliminating the threat of a huge fire. Thus, our group decided to create a device with the help of AI On Edge to help to detect for fire and riots. Due to the sheer speed of edge devices, it can quickly receive and send data to IBM cloud to alert the SCDF officials.

## Pitch video

[![Watch the video](put image here)](video link here) (need change)

## The architecture

![Video transcription/translation app](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/Architecture.JPG)

1. Fire is first detected by the Sipeed Module
2. The information is then send to an esp32 connected to the Sipeed Module
3. The esp32 will send the data to IBM Watson 
4. IBM Watson will send a push notification to the authoratives

## Long description

[More detail is available here](DESCRIPTION.md)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system. 

### Prerequisites

What things you need to install the software and how to install them

```bash
dnf install wget
wget http://www.example.com/install.sh
bash install.sh
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be, for example

```bash
export TOKEN="fffd0923aa667c617a62f5A_fake_token754a2ad06cc9903543f1e85"
export EMAIL="jane@example.com"
dnf install npm
node samplefile.js
Server running at http://127.0.0.1:3000/
```

And repeat

```bash
curl localhost:3000
Thanks for looking at Code-and-Response!
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why, if you were using something like `mocha` for instnance

```bash
npm install mocha --save-dev
vi test/test.js
./node_modules/mocha/bin/mocha
```

### And coding style tests

Explain what these tests test and why, if you chose `eslint` for example

```bash
npm install eslint --save-dev
npx eslint --init
npx eslint sample-file.js
```

## Built with

### Sipeed M1

Sipeed M1 is an open source AI development kit. It is useful in image recognition and any AI application. At the heart of the Sipeed M1 platform is the AI chip K210 by Kendryte, a dual-core RISC-V with an FPU. It serves as the core unit and dual-core processing with independent FPU, 64-bit CPU and 8M in-built SRAM. With a 400Mhz adjustable nominal frequency it supports multiplication, division and square root operation. The Sipeed M1 also integrates Micropython to make development pretty smooth and straightforward. With its edge computing capabilities, it can improve response time.

The Kendryte K210 is a system-on-chip (SoC) that integrates machine vision and machine hearing. Using TSMC’s ultra-low-power 28-nm advanced process with dual-core 64-bit processors for better power efficiency, stability and reliability. The SoC strives for ”zero threshold” development and to be deployable in the user’s products in the shortest possible time, giving the product artificial intelligence. Kendryte K210 is intended for the AI and IoT markets, but is also a high-performance MCU. Kendryte in Chinese means researching intelligence. The main application field of this chip is in the field of Internet of Things. The chip provides AI solutions to add intelligence to this.
- Machine Vision
• Machine Hearing 
• Better low power vision processing speed and accuracy 
• KPU high performance Convolutional Neural Network (CNN) hardware accelerator 
• Advanced TSMC 28nm process, temperature range -40°C to 125°C
• Firmware encryption support 
• Unique programmable IO array maximises design flexibility 
• Low voltage, reduced power consumption compared to other systems with the same processing power 
• 3.3V/1.8V dual voltage IO support eliminates need for level shifters

1.1   AI solution 

- 1.1.1 Machine Vision With machine vision capabilities, the Kendryte K210 is a zero-threshold embedded machine vision solution. It can perform convolutional neural network calculations with low power consumption. Capabilities: • Object Detection • Image Classification • Face Detection and Recognition • Obtaining size and coordinates of target in real time • Obtaining a type of detected target in real time 

- 1.1.2 Machine Hearing The Kendryte K210 has machine hearing capabilities. The chip comes with a high performance microphone array audio processor for real-time source orientation and beamforming. Capabilities: • Sound source orientation detection • Sound Field Imaging • Beamforming • Voice Wake-Up • Speech Recognition 

- 1.1.3 Hybrid Audio/Vision Solution The Kendryte K210 combines machine vision and machine hearing to provide even more powerful features. In the application, both the sound source localization and the sound field imaging can be used to assist the machine vision to track the target, and the general target detection can obtain the target’s orientation and then assist the machine to perform the beamforming of the source. Additionally, the direction of the person can be obtained by the image transmitted from the camera, so that the microphone array is directed to the person by beamforming. At the same time, the direction of speech can be determined according to the microphone array, and the camera is rotated to point to the person.

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

## Authors

* **Ashwin Dinesh**  
* **Lim Zi Xiong**  
* **Rusyaidi Bin Abdul Rashid**  
* **Chew Liang Zhi**  

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details



