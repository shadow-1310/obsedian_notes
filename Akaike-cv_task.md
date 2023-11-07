## Libraries used
- openCV
	- for image manipulation
- numpy
	- linear algebra operations

## workflow
- original image and the annotated image have different resolution.
- so original image is converted to same resolution as fully annotated image by doing centre crop
- then absolute difference between both the images is taken, which gives the mask of annotation over cat and dog
- Finally mask of dog is removed from fully annotated image to get a partially annotated image