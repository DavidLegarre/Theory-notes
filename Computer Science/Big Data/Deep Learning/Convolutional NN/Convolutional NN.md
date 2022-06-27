# Convolutional Neural Networks
Convolutional neural networks are a specialized type of artificial networks that use [[Convolution|convolutions]]  in order to extract feature maps from the image, from which later the net will try to find features that show the location of an object or any other purpose.

> Reference to pytorch library cheat sheet: [[Pytorch Cheat Sheet]]


## Architecture of a traditional CNN
![[Pasted image 20220518232903.png]]

## Types of layers
### The convolution layer (CONV)
The convolution layer (CONV) uses filters that perform [[Convolution]] operations as it is scanning the input $I$ with respect to its dimensions. Its hyperparameters include: the filter size $F$, and the stride $S$. The resulting output $O$ is called *feature map* or *activation map*.
![[convolution-layer-a.gif]]

> The convolution step can be generalized to the 1D and 3D cases as well.

### Pooling (POOL)
The pooling layer (POOL) is a downsampling operation, typically applied after a convolution layer, which does some spatial invariance. In particular, max and average pooling are special kinds of pooling where the maximum and average value is taken, respectively.

![[Pasted image 20220518233926.png]]


### Fully connected (FC)
The fully connected layer (FC) operates on a flattened input where each input is connected to all neurons. If present, FC layers are usually found towards the end of CNN architectures and can be used to optimize objectives such as class scores.
![[Pasted image 20220518234103.png]]
## Filter Hyperparameters
The convolution layer contains filters for which it is important to know the meaning behind its hyperparameters.

### Dimensions of a filter
A filter of size $F\times F$ applied to an input containing $C$ channels is a $F\times F\times C$ volume that performs convolutions on an input size $I\times I\times C$ and produces an output feature map (also called activation map) of size $O\times O\times 1$. 
![[Pasted image 20220518234308.png]]
### Stride
For a convolutional or a pooling operation, the stride $S$ denotes the number of pixels by which the window moves after each operation
![[Pasted image 20220518234628.png]]

### Zero-padding
Zero-padding denotes the process of adding $P$ zeroes to each side of the boundaries of the input. This value can either be manually specified or automatically set through one of the three modes detailed below:

![[Pasted image 20220518234659.png]]

## Tuning hyperparameters
### Parameter compatibility in convolution layer
By noting $I$ the length of the input volume size, $F$ the length of the filter, $P$ the amount of zero padding, $S$ the stride, then the output size $O$ of the feature map along that dimension is given by:

$$
O=\frac{I-F+P_{start}+P_{end}}{S}+1
$$
![[Pasted image 20220518235507.png]]

![[Pasted image 20220518235534.png]]

The output size of the pooling layer is calculated as:
$$
Floor\left(\frac{I-F}{S}+1\right)
$$
