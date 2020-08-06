# Face Recognition

-  Face recognition + liveness detection to avoid identifying printed  images

  ![image-20200725091814871](image-20200725091814871.png)

#### One Shot Learning

![image-20200725132924214](image-20200725132924214.png)

![image-20200725140021334](image-20200725140021334.png)

## Siamese Network[image-20200725191804830](image-20200725191804830.png)

![image-20200725191840729](image-20200725191840729.png)

And I'm going to give this list of 128 numbers a name. I'm going to call this f of x1, and you should think of f of x1 as an encoding of the input image x1. So it's taken the input image, here this picture of Kian, and is re-representing it as a vector of 128 numbers. The way you can build a face recognition system is then that if you want to compare two pictures, let's say this first picture with this second picture here. What you can do is feed this second picture to the same neural network with the same parameters and get a different vector of 128 numbers, which encodes this second picture. So I'm going to call this second picture.

![image-20200725192037377](image-20200725192037377.png)

### Triplet Loss

![image-20200725201616765](image-20200725201616765.png)

to make sure it dosent give encoding of zero as output  , we modify it to be compared to + alpha 

![image-20200725201814421](image-20200725201814421.png)

by adding the value it pushes the anchor values away from each other  

![image-20200725202417323](image-20200725202417323.png)

![image-20200725202617833](image-20200725202617833.png)

choose hard triplets for better training  , source paper listed below on facenet

![image-20200725202656802](image-20200725202656802.png)

![image-20200725202929228](image-20200725202929228.png)

### Face Verification and Binary Classification

Turning triples loss function into the binary classification problem ,using logistic regression to classify  it into either zero or one , 

Vide : https://www.youtube.com/watch?v=GWa9xsMU0Pg

![image-20200727114747692](image-20200727114747692.png)

Precompute the values so that  you dont have to calculate the values everytime 

## Neural Style Transfer

-  transfer the style from one image to the another images

  ![image-20200727130809602](image-20200727130809602.png)

## What are deep ConvNets learning?

![image-20200727160103834](image-20200727160103834.png)

to find how what activates the hidden units , deeper layer have more clear idea and understanding

![image-20200727160349637](image-20200727160349637.png)

## Cost Function for Neural Style Transfer

![image-20200727161006235](image-20200727161006235.png)

![image-20200727161134921](image-20200727161134921.png)

## Content Cost Function

![image-20200727162124325](image-20200727162124325.png)

## Style Cost Function

![image-20200727162451691](image-20200727162451691.png)

![image-20200727162616984](image-20200727162616984.png)

![image-20200727162804789](image-20200727162804789.png)

![image-20200727162825502](image-20200727162825502.png)

#### 1D and 3D Generalizations

![image-20200727164504430](image-20200727164504430.png)

![image-20200727164947995](image-20200727164947995.png)