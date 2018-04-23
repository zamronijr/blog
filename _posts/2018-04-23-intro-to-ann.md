---
layout: post
section-type: post
title: Intro to Artificial Neural Network
category: tech
tags:
  - tutorial
published: true
---
Neural network is a model that is inspired by how neurons in the human brain work. Each neuron in the human brain is interconnected and information flows from each neuron. The picture below is a neuron illustration with its mathematical model.
![ann1.jpg]({{site.baseurl}}/img/ann1.jpg)
Each neuron receives input and performs a dot operation with a weight, adds it (weighted sum) and adds bias. The result of this operation will be the parameter of the activation function that will be the output of the neuron.
#### Activation Fucntion
As the name implies, the activation function functions to determine whether the neuron should be "active" or not based on the weighted sum of the input. In general there are 2 types of activation function, Linear and Non-Linear Activation function.
![ann2.jpg]({{site.baseurl}}/img/ann2.jpg)
It can be said that the "default" activation function of a neuron is Linear. If a neuron uses a linear function, then the output of the neuron is the weighted sum of the input + bias.
![ann3.jpg]({{site.baseurl}}/img/ann3.jpg)
Sigmoid function has a range between 0 to 1 while the range from Tanh is -1 to 1. Both of these functions are usually used for classification of 2 classes or groups of data. But there are disadvantages of these two functions.
![ann4.jpg]({{site.baseurl}}/img/ann4.jpg)
Basically ReLU performs a "treshold" from 0 to infinity. ReLU can also cover the weaknesses possessed by Sigmoid and Tanh
#### Neural Network Architectures
![ann5.jpg]({{site.baseurl}}/_posts/ann5.jpg)
The above architecture is commonly referred to as Multi Layer Perceptron (MLP) or Fully-Connected Layer. The first architecture has 3 neurons in the Input Layer and 2 Output Layer nodes. Among Inputs and Outputs, there is 1 Hidden Layer with 4 neurons. While the Weight and Activation function specifications are as follows:
##### Weight and Bias
Each neuron in the MLP is interconnected which is marked by arrows in the image above. Each connection has a weight that will be the value of each weight will vary.
Hidden layer and output layer have additional "input" commonly called bias (Not mentioned in the picture above).
So in the first architecture there are 3x4 weight + 4 bias and 4x2 weight + 2 bias. Total is 26 parameters that the training process will undergo changes to get the best result. While on the second architecture there are 41 parameters.
##### Activation Function
Neurons in the input layer do not have activation function, while neurons in hidden layer and output layer have activation function which sometimes differ depending on data or problem that we have.
#### Training a Neural Network
In Supervised Learning using Neural Network, in general, Learning consists of 2 stages, namely training and evaluation. But sometimes there is an additional stage of testing, but its not mandatory.
At the training stage each weight and bias on each neuron will be updated continuously until the output produced in accordance with expectations. At each iteration will be a process evaluation which is usually used to determine when to stop the training process (stopping point)
The training process consists of 2 stages:
- Forward Pass
- Backward Pass

