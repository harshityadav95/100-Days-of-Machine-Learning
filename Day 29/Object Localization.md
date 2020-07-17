## Object Localization 

- Object detection starts with object localization
- Localization :  Identifying and marking object in the Image which is in middle and visible clearly  
- In detection multiple objects of that type will be visible in the example image
- Bounding Box of highlighting the area of the images 

![image-20200714080823946](image-20200714080823946.png)



![image-20200714085648805](image-20200714085648805.png)

### Sliding Window detection

used earlier with linear function and classifier , but convnets this way is slow

![image-20200714090429430](image-20200714090429430.png)

solution 

- Convert fully connected layer to convolution layers

  ![image-20200714090832110](image-20200714090832110.png)

![image-20200714091507512](image-20200714091507512.png)

Computationally expensive and not accurate

### Bounding box Prediction - YOLO

![image-20200714125248009](image-20200714125248009.png)

Finding the mid point of the object and then deciding which  grid cell it belongs too

![image-20200714125754477](image-20200714125754477.png)

YOLO is a tough paper to understand 

## Intersection over Union

![image-20200714130440974](image-20200714130440974.png)

Using Intersection of actual and output localization to check for accuracy 

## Non Max supression

to solve the problem of detecting the same object multiple times in an image ,by looking at high probability localization and then one with high overlap get supressed (suppress that are non max)

![image-20200714193806250](image-20200714193806250.png)

 ## Anchor Boxes to solve overlapping objects

![image-20200715200147034](image-20200715200147034.png)

![image-20200715200327720](image-20200715200327720.png)

## Yolo Algorithm

![image-20200716164227779](image-20200716164227779.png)

![image-20200716171902983](image-20200716171902983.png)

## Region Proposal (optional)

- Run a segmentation algorithm  

  ![image-20200716172240077](image-20200716172240077.png)

![image-20200716172534511](image-20200716172534511.png)