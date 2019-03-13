---
title: "Deep Action Conditional Neural Network for Frame Prediction in Atari Games"
excerpt: ""
collection: portfolio
paperurl: 'https://ewang314.github.io/files/frame-prediction-cs231n.pdf'
date: 2017-06-01
citation: '**Wang, E.**, Kosson, A., Mu, T. Deep Action Conditional Neural Network for Frame Prediction in Atari Games. *Stanford CNNs for Visual Recognition (CS 231N) Project*, 2017'
---
Abstract
======

In many problems in computer vision and video frame prediction, such as in robotic control or self driving cars, future frames are not only dependent on past frames, butalso on external actions. We study this problem by looking at video frame prediction in the context of Atari 2600 video games where future frames are dependent on past frames as well as actions performed by the players. Based off of previous work, we implement a convolutional feed-forward model for predicting future frames and rewards as well as a baseline multi-layer perceptron (MLP). We test various training schemes including using an autoencoder to improve prediction clarity and using different loss functions such as the l2 loss, the l1 loss, and the Structural Dissimilarity (DSSIM). We generate data by collecting frames and rewards from a Deep Q Network (DQN) trained to play the game. We found that both quantitatively and qualitatively the convolutional feed-forward model achieves better results than the MLP.
{: .text-justify}
