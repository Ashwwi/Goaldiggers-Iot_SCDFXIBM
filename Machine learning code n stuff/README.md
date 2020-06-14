# Machine learning 

we used the speed m1 dock
u might be asking why compared to a rasberry pi well it comes down to the hadware the speed m1 
doc has K210 ai aceelater chip wich helps alot in machine vision/audio processing  and it uses the open source risc-v architecture  which is very efficent for processing risc-v stands for *reduced instruction set 5*  this enables us do edge computing u can see a video demo here :
<img src="https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/Machine%20learning%20code%20n%20stuff/machine%20test.gif">
<img src="https://github.com/Ashwwi/Goaldiggers-Iot_SCDFXIBM/blob/master/Machine%20learning%20code%20n%20stuff/IMG_20200614_142252.jpg">
to process the data we used data set that was alerady trained because of the limitations of the scdf challange we didnt have enough time to individually look through more that 1000 images we then trained the model in tensor flow and converted it tensorflow lit and then converted it into kmodel file wich the k21o use to process the code is written in micropython which again enabled us to do quick testing 

