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

