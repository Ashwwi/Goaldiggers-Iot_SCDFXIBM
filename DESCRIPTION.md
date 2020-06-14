# Anomalies detection with Sipeed MAIX KD210

## Training the device

Training the model for AI@Edge with the KD210 device

The KD210 device will be fitted with a machine learning model that is able to detect anomalies, such as gathering of human, fire, and suspiciosn behaviour.

This is important step to train the model as we would like to make it as accurate as possible to not activate more precious emergency resources due to false positive. 

Some prerequsites required are python 3.6, tensorflow, keras and opencv. 
Installation: pip install tensorflow pip install keras pip install opencv

To run a pre train model, maixhub is kind enough to provide us with facial recognition model for us to learn about the process. Due to time constraint, we are using the pretrained model from maixhub for facial recognition. 

In future, we will be traning the model for fire, and crowd gathering

Alternatively if you want to run a pre train model, maixhub is kind enough to provide us with model and due to time constraint, we are going to load from maixhub to grab a trained model head to maixhub.com and download the pretrained model.

### Loading the model
Before loading the model, we need to retrieve the machine code and flash it to the device to do this, we download the the first keygen firmware from https://en.bbs.sipeed.com/uploads/default/original/1X/bca0832bed92a1ada63bd05327688784e2ef14d1.zip and unzip.

After unzipping you will get a bin file. Next, we need to download kflash from https://github.com/sipeed/kflash_gui/releases/tag/v1.5.3 in order to flash the device with the machine code.

Once we flash the device, open up the serial terminal and the second sentence will be the machine code. Note down the machine code.

Next up, we download the model from maixhub.com we selected facial recognition but you can choose your prefered model to run. To download you have to register an account. You will be prompted to key in something and this is where you input your machine code inside. Once you inputted the right machine code, the download will start.

To load the model, we open up kflash and flash the dpkg file we downloaded in the previous step. After the flashing is complete, the development board displays the MaixPy welcome interface. And you should see the model running.

## Test
To test simply flash the camera with a face(it can be more than 1) and the you should see that the sipeed is able to detect the face.


## Conclusion

In this guide, we learn how to load a pretrained model from maixhub into sipeed maix bit.

## Acknowledgments

https://blog.sipeed.com/p/1338.html
