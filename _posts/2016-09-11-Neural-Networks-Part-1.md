---
title:  "Neural Networks Part - 1"
date:   2017-09-11 15:04:23
comments: true
categories: Introduction Artificial Intelligence
tags: AI ML Intro
---


This article is one of the series of articles on neural networks.
 - Neural Networks intro (this article)
 - Loss function
 - Activation function

So you have started with Machine Learning and went through pretty much every short tutorial on how everything works and what to do to get started. But still, there might be a gap in your understanding of the exact mechanism of how neural networks internally work.

You must have come across some of the words like **Backpropagation, Regularization, Activation Function**, etc. But never really understood the math behind these. It’s a lot easier to code your own neural network when you can visualize the underlying processes and how things flow through the network.

## Neural Network
![4 Layer Neural Network](https://cdn-images-1.medium.com/max/880/1*cemKtt3xPbXyH2dyr892sg.png "4 Layer Neural Network"){:class="img-responsive"}

Your neural network takes an input x (Vector of size 3 here) and outputs a single number y. Here you can imagine any example that can have 3 inputs and 1 output. Like predicting whether or not you will receive a loan from a certain bank based on your features such as your salary, age and asset value. This type of problem is called classification. When the inputs are numbers and output is one of the classes.

Here xᵢⱼ is the jᵗʰ neuron in iᵗʰ layer. Each neuron has 4 components. Input vector, weights vector, bias and an activation function. Let’s zoom into one of the neurons, say x₂₁

![Neuron X₂₁](https://cdn-images-1.medium.com/max/880/1*2-r82S0K1JTYfTmk295YHg.png "Neuron X₂₁"){:class="img-responsive"}

## Functions of a Neuron

1. Takes inputs from the previous layers and keeps it in a vector of size = number of neurons in previous layer.
2. Has some weights in a vector of size = number of neurons in previous layer. These weights can be initialized to a random number. (There are a lot of techniques to initialize these weights which will improve the training of the network. Here we will initialize them to a random number for simplicity.)
3. Has a bias component. It is a scalar value.
4. It computes the sum as


![](https://cdn-images-1.medium.com/max/880/1*mTVtLnEIHXI-A8dRkMd0Kg.png){:class="img-responsive"}

5. The output of a neuron is given by its activation function. There are many options to choose from, for this function. The one used here is called a sigmoid function. It crunches down the x to a number between 0 and 1. Explanation of sigmoid and other options can be found [here](https://medium.com/towards-data-science/activation-functions-and-its-types-which-is-better-a9a5310cc8f).


## Training a Neural Network
Things you’ll need to train a neural network are :
1. The network itself. As we defined above. Weights on each of the neuron are initialized to a random value.
2. Training data. It consists of (x,y) pairs where x is the input vector of size 3 here, and y is the result corresponding to that x vector.

In the next part, we’ll have a look at the loss function that will be used for estimating performance of our model.