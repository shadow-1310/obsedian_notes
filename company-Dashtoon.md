things that the company is working on
- Building a consistent character universe that can be used by creators.
- Baking composition of a scene into the AI models.

working towards
- Alignment: Fine-tune models to perform tasks per the creator's intentions. Explore learning from human feedback or assisting humans.
- Scaling: Build the model training software stack, solving problems at all layers of the stack, including iteration speed, observability, compute efficiency, correctness, and fault detection and recovery. Scaling owns the engineering and research required to harness the latest algorithmic improvements and datasets to train AI models of unprecedented capability.

https://www.youtube.com/watch?v=8pp0Oa3t52s&list=PLBoQnSflObcmbfshq9oNs41vODgXG-608&index=4
https://www.kaggle.com/code/yashchoudhary/fast-neural-style-transfer

https://github.com/gordicaleksa/pytorch-neural-style-transfer

A/B testing
- sampling, how to sample
- SUTVA, doesn't hae bias
- hypothesis testing
- Bayesian Testing


Gaurang -- Flipkart, Navi, EdgeVerse
Yeturi - Micron, Samsung, Infoedge

interpolation techniques
- nearest neighbour
- bilinear
	- linear weighted average
- bicubic
	- find a eqn of a polynomial line between 2 points using position and gradient.
### Built in modules
- Conv2D
	- arguments
		- input channel
		- output channel
		- kernel size
		- stride
- InstanceNorm2D
	- args
		- out channel
		- affine
## ConvBlock
- Args
	- in_channels, 
	- out_channels, 
	- kernel_size, 
	- stride=1, 
	- upsample=False, 
	- normalize=True, 
	- relu=True
- instance variables
	- self.block
		- Refelction Padding
		- Conv2d
	- Instance Normalization
	- relu
-  forward method
	- upsample, interpolation
		- nearest, default
			- options - bilinear, bicubic, 
	- block
	- instance normalization
	- relu

## Residual Block
- Args
	- channels
- instance variable
	- self.block
		- convblock
		- convblock
- forward method
	- self.block(x) + x

## How to get
- Transformed image
	- train image
		- resize , 1.5 times
		- random crop, this step is for data augmentation.
		- to tensor 
		- normalize
	- style image
		- resize
		- to tensor
		- normalize, with mean and std of ImageNet
	- Deprocessing
		- multiply with std of that channel and add mean of that channel.
		- multiply with 255
		- clamp inside (0, 255), torch.clamp
			- convert to numpy, 
			- save to cpu
			- set datatype to np.unint8
			- transpose(1,2,0), change the format from [channels, height, width] to [height, width, channels]
				- because pytorch/tensorflow handles image matrix different from opencv, matplotlib
- Gram Matrix
	- get shape of the layer
	- flatten the w* h into a single array
	- find its transpose
	- find gram matrix by $AA^{T}$
	- divide this by c* h * w for normalization across all the feature channels.