### Alex Net
---
important features
- overlapped pooling, 3x3 kernel with stride 2(usually we use 2x2 kernel with stride 2)
- Layer Normalization
- ReLU 
- Dropouts 
- Data Augmentation
- training was done on 2 GPUs by splitting the architecture
##### important questions
- why use 224x224 input

## VGG Net (Visual Geometry group)
---
[nptel video](https://www.youtube.com/watch?v=GrLaytcy15M)
uniqueness over previous models
- introduced the block system in architecture
- succession of layers of smaller kernel can act as an larger kernel with less parameters, 
	- because 2nd layer will see 5x5 of the original input image
- 