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
![ann1.jpg]({{site.baseurl}}/_posts/ann1.jpg)
Each neuron receives input and performs a dot operation with a weight, adds it (weighted sum) and adds bias. The result of this operation will be the parameter of the activation function that will be the output of the neuron.
#### Activation Fucntion
As the name implies, the activation function functions to determine whether the neuron should be "active" or not based on the weighted sum of the input. In general there are 2 types of activation function, Linear and Non-Linear Activation function.
![ann2.jpg]({{site.baseurl}}/_posts/ann2.jpg)
It can be said that the "default" activation function of a neuron is Linear. If a neuron uses a linear function, then the output of the neuron is the weighted sum of the input + bias.
