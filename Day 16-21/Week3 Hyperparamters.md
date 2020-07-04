## Tuning Process

Hyper parameters that can be tuned  

- Alpha 
- Beta (momentum term)
- beta1, beta2, epsilon 
- Number of layers
- Hidden Units  
- Learning rate decay
- mini batch size  



Order of choosing the right hyper parameter while tuning a model

1. alpha 
2. momentum term , and mini batch size  and hidden units are
3. number of layers and learning rate decay are 



Try Random values of hyper parameters and don't follow the grid method and randomly chosen points , some hyper parameter might be more important than other the other in your project so decide them according to your need , move from coarse to more fine tuning  your sample values while searching 

## Using  Appropriate scale to pick hyper parameters 

Search for hyper parameter values on the log scale randomly than a linear scale

Take the high value, take a log to figure out what is b. So now you're trying to sample, from 10 to the a to the b, on a log scale. So you set r uniformly, at random, between a and b. And then you set the hyperparameter to be 10 to the r. 

Hyperparamters for exponentially weighted averages b



## Hyperparameter tuning in practice : pandas vs Caviar

Re-Test Hyper-parameters occasionally , on production or even fixed model

Babysitting the model of single model is good when not having the lot of computation

Training models in parallel  is good when  having lot of computation



## Normalizing activation in a network 

Normalizing helps in faster learning 

Batch Normalization  is normalize your data set according to the variances , the value should not be cluttered and have wide variance based on value beta and gamma



## Fitting Batch Norm into a Neural Network

Using inbuilt framework optimization to get results



## Why does Batch Norm Works  

 Batch norm reduce the amount of coupling between the layers , and makes learning in later layers easier

It has a slight regularization effect  , dont use it there are unintended side affects and need larger batch size otherwise its more noisy



## Softmax Regression

 The  number of neurons in the last /output layer is equal to the number of classification  

Descion Boundary between the softmax functions is linear

- Softmax layer



## Tranining softmax classifier

Gradient descent with softmax : Apply softmax activation function 







