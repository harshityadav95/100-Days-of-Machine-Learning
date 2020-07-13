# Convolution Neural Network

#### computer vision and edge detection 

- Edge detection  

  Earlier layer detect images  - > Later Features and then -  > More advanced Features

- Edge Detection using the Filter

- Vertical edges is gap betwenn dark and light pixel  using the filter (Horizontal and vertical edge detection)

- Edge detector filter parameter are trained as weights of NN 

- NN can learn better to handle all types of the filter at every angle rather than manually setting them  

- Formula used for Padding  in images  

- Same padding -  > output size is same as input size 

- Valid Padding  -> Change the size of the output image 

- Strided Convolution : moment of filter on top of image

- Convolution in RGB channel   , filter for each channel in each layer  

  ![image-20200710131938801](image-20200710131938801.png)

- can use same filter in all 3 channel or in particular color only

  ![image-20200710132400415](image-20200710132400415.png)

## One layer of a convolutional network

![image-20200710142407435](image-20200710142407435.png)

Q . 10 filter (3x3X3)  , total number of paramters 3^3+1(bias)=28

 ![image-20200710183209025](image-20200710183209025.png)

![image-20200710192338040](image-20200710192338040.png)

- Convolution layer and pooling layer is single layer

- As you go deeper the height and with will decrease but channels will increase

- Pooling layers dont have any parameters

- Activation size also goes down slowly  

  ### WHy convolutional Layers  ?

  - the number of paramets is too large othewise 

    the number of parameters in a weight matrix would be 3,072 

    times 4,704 which is about 14 million

![image-20200711083450620](image-20200711083450620.png)

- Parameter sharing - using same filter for different edges 
- Sparsity connection - only few parameters needed at a time

![image-20200711083641257](image-20200711083641257.png)

## The basics of ConvNets

In lecture we talked about “parameter sharing” as a benefit of using convolutional networks. Which of the following statements about parameter sharing in ConvNets are true?

- It allows a feature detector to be used in multiple locations throughout the whole input image/input volume.
- It reduces the total number of parameters, thus reducing overfitting.

- Convolution functions, including:
  - Zero Padding
  - Convolve window
  - Convolution forward
  - Convolution backward (optional)
- Pooling functions, including:
  - Pooling forward
  - Create mask
  - Distribute value
  - Pooling backward (optional)

![image-20200711113151502](image-20200711113151502.png)

The main benefits of padding are the following:

- It allows you to use a CONV layer without necessarily shrinking the height and width of the volumes. This is important for building deeper networks, since otherwise the height/width would shrink as you go to deeper layers. An important special case is the "same" convolution, in which the height/width is exactly preserved after one layer.
- It helps us keep more of the information at the border of an image. Without padding, very few values at the next layer would be affected by pixels as the edges of an image.



### Case Studies

- LeNet-5
- ![image-20200712123653916](image-20200712123653916.png)
- AlexNet

 ![image-20200712124247719](image-20200712124247719.png) 

- VGG -16 

![image-20200712130954258](image-20200712130954258.png)

- ResNet

![image-20200712132421148](image-20200712132421148.png)

![image-20200712132656830](image-20200712132656830.png)

![image-20200712133556702](image-20200712133556702.png)

![image-20200712140428207](image-20200712140428207.png)

## 1x1 convolution

![image-20200712191633788](image-20200712191633788.png)

 

![image-20200712200458499](image-20200712200458499.png)



![image-20200712202951676](image-20200712202951676.png)

- Inception NN

![image-20200712203714383](image-20200712203714383.png)

![image-20200712203943947](image-20200712203943947.png)

![image-20200712204218596](image-20200712204218596.png)

- Inception Module
- Inception Network , GoogleNet



## Practical Advice for using ConvNets

- Use github and author  implementation of the code  

## Transfer Learning  

- Using pre trained weight from one model to train another whose data is not much available to train 

  

## Data Augmentation 

- changing the existing data with more color and cropping and rotation to generate the new data  for training  for the dataset
- PCA color augmentation 
- Distortion , can be done via cropping  , mirroring  , rotation  , color  change  



## State of Computer Vision 

For doing well on benchmarking. winning competition , not for production system

- Ensembling 

- Multi Crop at test time 

  







