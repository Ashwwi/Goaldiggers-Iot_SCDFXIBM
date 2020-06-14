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

Fire occurs everywhere in the world. They are unavoidable but preventable. As such, fire prevention measures are taken to reduce the risk. However when fires occur, they can have a detrimental impact on the environment if not taken care of swiftly. As such reactive solutions  (Needs work)

### How can technology help?

Technology can play a big part in fire detection. Machines are faster than the average human reaction thus utilizing that speed can be beneficial in detecting fires. (Needs work)

### The idea

Detection is key in eliminating the threat of a huge fire. Thus, we decided to create a machine learning model that is able to detect fires. The model is able to identify when a fire has started and broadcast this critical information to the authoratives in a matter of seconds. 

## Pitch video

[![Watch the video](put image here)](video link here) (need change)

## The architecture

![Video transcription/translation app](https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/resources/Fire%20Detection.JPG)

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


