# E-waste-managment
HackNITR

**ABSTRACT**

**Data Collection**


   We discovered that there was a dearth of annotated, high-quality e-waste imagery data when we searched for it.
   We have used:
1.	Version 3 of Starter: e-waste dataset 93b07fb8-a from kaggle as it contained images in 4 category:

              1.	Keyboard
              2.	Mouse
              3.	Laptop
              4.	Monitor/Television
              5.	Mobile
    We used its 3rd version as upgraded versions contained images of plastic bottles also. Which were not meant to our model.
    

2.	As data collected was not sufficient we got data for keyboard, laptop and monitor form images.cv

**Design of Model**


**Tried simple cnn**

•Firstly we used a simple convolution neural network with 3 layers of 2D Maxpooling extracting 16 ,32 and 64 filters. Used an output layer with softmax activation function.
With limited data and without dropouts and early stopping the model got over fitted with large difference between training accuracy(0.9600) and validation accuracy(0.5102)

**Applied VGG19 Model**

•In simple language VGG is a deep CNN used to classify images. There are 19 weight layers in VGG19 model. A fixed size of (224 * 224) RGB image was given as input to this network.

**Implementation**

•	We had data in 5 classes ({'keyboard': 0, 'laptop': 1, 'mobile': 2, 'mouse': 3, 'television': 4}) so we divided the whole data into train, test and validation dataset.

•	Then reshaped the data into (224x224) for input in vgg network.

•	To prevent weight changes throughout epochs, we placed the trainable layers in vgg to false or freeze. 

•	We applied early stopping for minimum validation loss.

•	Next, we trained the model for 10 epochs.

•	Refer to notebook for detailed explanation.
            
**Deployment**

The model deployment
-vg99 deep learning model

**Description of the web application**

The web application uses simple techniques for its implementation.

- **HTML & CSS** for the frontend part.
- **Flask** is used in backend.

**Observation**

•Got 100% train accuracy and 94.90% validation accuracy with 0.1521 validation loss.

 ![img111](https://user-images.githubusercontent.com/111306079/211804409-2e7888b2-fd80-4657-8cf4-4563a2847f37.png)

•Accuracy for training and validation data

 ![img222](https://user-images.githubusercontent.com/111306079/211804658-27653656-7e95-447e-9f80-c932fb7c4ed5.png)

Loss for training and validation data
