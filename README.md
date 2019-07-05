# ML-starter-problems
This repository contains a collection of problems to help new people enter the field of deep learning for computer vision.\
We provide below a list of problems to start with, along with a short description.\
\
If you have solved a problem, please open a pull request. A solution will contain both code and a brief explanation of the procedure followed.

## Challenge #1: AI-based compression

This challenge is a toy problem to warm up to AI-based compression. This challenge composes of several steps, each is a quantum jump more difficult/more computational demanding compared to a previous one.\
\
(a) Randomly generate a set of vectors. Each vector has 64 pixels organized in a row. The value of pixel 0 to pixel L is 0.0, of pixel L+1 to R is 1.0, of R+1 to 63 is 0.0. This is a dataset of one-dimensional black-and-white "images".\
\
(b) Define a CNN-based autoencoder (of any kind) that takes in and reproduces the above images. Show us how well you are doing. Can your network perfectly reproduce the input? What is the minimal cardinality of the bottleneck layer? You must select the parameters properly, so that the network does not learn the trivial solution.\
\
(c) If you are not satisfied with the result in (b), can you improve upon it? Perhaps you surmise that it is the architecture that is the problem. In which case you can seek a non-CNN solution. For instance, you may try fully connected networks, or self-attention networks. Perhaps you surmise that it is a lack-of-information issue. In which case you might feed the network additional information to help it learn. For instance, you might try the coordinate convolution trick.

## Challenge #2: AI-based generation

This challenge is a toy problem to warm up to AI-based generation. This challenge composes of several steps, each is a quantum jump more difficult/more computational demanding compared to a previous one.\
\
(a) Pick at your own whim a stochastic random process that can generate a time-varying sequence of 16-dimensional vectors. You will use this to generate ground truth.\
\
(b) Give a discriminator which takes in two vectors and determines whether it is plausible that the second vector follows the first vector.\
\
(c) Give a generator that takes in vector n and generates an output vector to fool the discriminator. That means, the discriminator should deem this fake vector to be a plausible vector n+1. Try to avoid trivial solutions.\
\
(d) Treat the networks in steps (b) and (c) as being given. Here we want you to try early rejection. That is, the generator in (c) operates in a layer-by-layer manner, advancing from the input layer to the output layer. Try to declare a given run of this generator will be rejected by the discriminator using some observation before the generator's final output layer.

## Challenge 3: Entropy from partial information in images

In MNIST each image has dimensions 28x28 and with each pixel represented by a grayscale value with range [0,255]. Rescale the images such that they are in the rate [1, 255].  For each pixel you can get do x <- min(x+1, 255). We will use 0 to represent an unknown value.  We can now generate images with unknown values programmatically or randomly by inserting zeros into each image.\
\
Train a network to predict probability distributions (categorical) of unknown pixels given an image that has unknown values.  After training the network, given an image that is completely unknown, which pixels have the highest entropy?  Can you propose and explanation for your results?


 
