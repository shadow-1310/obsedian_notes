UnNormalized Cross Covariance
- [youtube video](https://www.youtube.com/watch?v=6KGtaXR7yMU)

Types of Style Transfer
- Artistic 
- Photorealistic

## History
- Signal processing and using filter, 1980s
- Image Analogies - Patch based technique, 2000s  
	- simulate brush stroke on real image.
- Neural Style Transfer - Optimization Method
	- Leon Gatys et. al, VGG-19 based network, 2015
	- https://arxiv.org/abs/1903.09760, WCT2 method
- Neural Style Transfer - Feed forward method
	- Justin Johnson et. al, 2016
	- Ulyanov et. al - instance normalization
	- Conditional Instance Normalization
		- generate images in different style by same convolutional parameters but different affine parameters in IN (Instance Normalization) layer
	- Controlling Perceptual factors in NST
		- Spatial control
		- color control
		- scale control
	- Arbitary style transfer in real time
	- Universal Style Transfer
	- Artistic Style Transfer for videos
		- ReCoNet - Real Time Video Style Transfer Net
#### Challenges of NST
- Aesthetic Evaluation for both NPR and NST
- No standard benchmark image set
- 

### Working
[good youtube video](https://www.youtube.com/watch?v=n1USIY_QuQc)
[blog](https://medium.com/machine-learning-algorithms/image-style-transfer-740d08f8c1bd)
- content representation
	- choose initial layer of CNN
	- define a loss matrix between feature maps of original image and target image.
	- Content Loss
		- MSE loss between same feature map of original image and target image.
- Style Representation
	- Gram matrix
		- Covariance Matrix between all the feature maps
		- https://www.youtube.com/watch?v=FQiNeuRqZu8
	- Style Loss
		- MSE loss between Gram Matrices
- Total Loss = $\alpha$ x Content Loss + $\beta$ x Style Loss

### Losses
- Loss = Content Loss + Style Loss
	- Content Loss
	- Style Loss -> Style Matrix -> Gram Matrix
	- Total Variation Loss (https://en.wikipedia.org/wiki/Total_variation_denoising)
### Impact of decisions
- initialization
	- initialize the target image with content/style/random
- choosing the layer of CNN for content loss
	- layer towards output gives 
### Codes


### Datsets
- [MIT Scene Parsing](http://sceneparsing.csail.mit.edu/)


#### Errors
- LBFGS closure error
	- https://sagecal.sourceforge.net/pytorch/index.html