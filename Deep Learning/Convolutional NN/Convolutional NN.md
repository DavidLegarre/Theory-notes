# Convolutional Neural Networks
Convolutional neural networks are a specialized type of artificial networks that use [[Convolution|convolutions]]  in order to extract feature maps from the image, from which later the net will try to find features that show the location of an object or any other purpose.

## Building blocks of a CNN

![[Pasted image 20220510213547.png]]

### 1. Convolutional layer

This layer is usually used at the beginning of the network to extract the feature maps, this layer consists of a set of trainable filters (or [[Convolution#Convolutional matrix|kernels]]). During the forward pass, each filter is convolved across the width and height of the input volume, computing the [[dot product]] between the filter and the input 