# Fire Detection
![Image]()
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

Technologies are able to play a big part in fire detection. Machines are faster than the average human reaction thus utilizing that speed can be beneficial in detecting fires. Our group decided to equip devices capable of detecting fires at many locations. The sipeed m1 module is used as our device as it was compact, easy to install and was able to achieve our goals. (Needs work)

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

* [IBM Cloudant](https://cloud.ibm.com/catalog?search=cloudant#search_results) - The NoSQL database used
* [IBM Cloud Functions](https://cloud.ibm.com/catalog?search=cloud%20functions#search_results) - The compute platform for handing logic
* [IBM API Connect](https://cloud.ibm.com/catalog?search=api%20connect#search_results) - The web framework used
* [Anaconda](https://www.anaconda.com/) - Python

## Authors

* **Ashwin Dinesh** - *Initial work* - 
* **Lim Zi Xiong** - *Initial work* - 
* **Rusyaidi Bin Abdul Rashid** - *Initial work* - 
* **Chew Liang Zhi** - *Initial work* - 

See also the list of [contributors](https://github.com/Code-and-Response/Project-Sample/graphs/contributors) who participated in this project.

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments


