---
layout: post
title: Automatically design your Tensorflow network with Chocolate
tags:
- machine learning
- tensorflow
- chocolate
- deep learning
- hyperparameters
---

Hyperparameters
===============

When you set up any learning model, whether it is a deep network or a
ridge regressor, there are usually parameters that the best
practitioners can use to add domain knowldege or tweak the performance
of the model. For example with a neural network, there are innumerable
parameters: the number of nodes in a layer, whether the layer uses
convolutions, how big those convolutions are, the regularization
strength, the learning rate, the learning algorithm and whether to
pre-whiten the inputs; among many others. These parameters are called
hyperparameers to distinguish them from the parameters that are set by
the training algorithm (normal parameters like the neural network
weights and biases).

Manual And Semi-Manual Tuning
==============

Choice of hyperparameters can be a very different kind of optimization
problem than that solved by the normal parameters. Frequently the
hyperparameters are categorical variables (like "which learning
algorithm") or discrete variables (like "number of nodes in a
layer"). And the hyperparameters can have deep and important
interactions: the larger the number of weights, the smaller the steps
your Stochastic Gradient Decent should take.

For many years, training was very expensive. So the default method of
setting hyperparameters was to do it by hand. A practitioner would
have years of experience that would allow them to guess what adequate
values of the hyperparameters would be: for example, use symmetric
layer-sizes around an auto-encoder's smallest layer.


However, in practical experience, if you have enough data it is better to peel off some of the data to

[TODO]: discuss why someone might want to choose a hyperparameter optimization framework and how chocolate solves those problems