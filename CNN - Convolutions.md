
[website of convolution animations](https://animatedai.github.io/)
Conv2D animation
- [good animation on youtube](https://www.youtube.com/watch?v=eMXuk97NeSI)

### Depthwise-separable Convolution (9 times more faster)
[ animation](https://www.youtube.com/watch?v=vVaRhZXovbw&list=PLZDCDMGmelH-pHt-Ij0nImVrOmj8DYKbB&index=6)
[theory](https://www.youtube.com/watch?v=T7o3xvJLuHk)
[tensorflow documentation](https://www.tensorflow.org/api_docs/python/tf/keras/layers/SeparableConv2D)
- Groups
	- separate group of kernel does convolve on different part of input feaures
- Depthwise Convolution
	- [tensorflow documentation](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D)
	- filtering stage
	- convolution on each channel separately
- Pointwise Convolution
	- combining stage
- Applications
	- XceptionNet
	- MobileNet
	- MultiModel Network