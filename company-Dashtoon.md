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


#### Data governance
- managing quality and security of data
API
- Application program interface

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
		- random crop, this step is for data augmentation. (to the required size)
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
				- because pytorch/tensorflow handles image matrix different from opencv, matplotlib.
- Gram Matrix
	- get shape of the layer
	- flatten the w* h into a single array
	- find its transpose
	- find gram matrix by $AA^{T}$
	- divide this by c* h * w for normalization across all the feature channels.
- Covariance vs gram matrix
	- for covariance we subtract the mean

##### Self-learning tasks
- yolov4
	- setup yolov4 on local
	- object detection on video
- yolov5
	- setup yolov5 on local
	- object detection
- how to use labelImg and bulk image downloader OIDv4 toolkit
- OIDv4 toolkit
	- https://github.com/EscVM/OIDv4_ToolKit
	- uses open image dataset
	- annotations will be fownloaded in csv file which can be easily converted to .txt file
- streamlit app for image transformation

## All tasks
- POCs
	- [[OCR for beverage client]]
		- main idea was to detect the important text area using green veg symbol as template
			- then we crop that area into specific sections of MRP, MFG, expiry batch no. and net quantity using cv2
			- we feed this small sections to YOLO model and get outputs for specific values
		- but as the photos were taken by hand using smartphone so we had to do the cropping task manually
		- and feed this cropped photos to the train model and take inference.
	- [[OCR of GRN sheet]]
		- grn sheet full of cells where each cells had separate entry.
		- at first easyOCR was not giving good results, so I processed the image with gimp and feed that image yolo
			- then I found out that the problem was with horizontal bar below, so I move my focus more towards removing horizontal bar.
				- so it was done in 3 steps
					- convert image to threshold/binary image
					- detecting the horizontal lines using horizontal kernel with opening operation
			- I also made a streamlit app to finetune the params required for processing
	- Sapling Count
	- hsv value comparison of different products
- Annotations tasks
	- bath towel
	- shaft count
	- bags
- 3D model tasks
	- [[Shaft Defect Detection]]
	- shrinkage detection in clothes
## Projects
---
### Vehicle Count
Workflow
- Data Ingestion
	- Open image dataset using OID toolkit
	- annotations are converted 
- Model training
	- yolov5 model is trained
- Detection
	- Load Models
	- load video
	- read frames
	- detect vehicle
	- track vehicle
	- detect license plate
	- assign license plate to vehicle
	- crop license plate
	- process license plates
		- convert to threshold/binary image inverted
	- detect and format license plate
		- detect text using OCR
		- check if matches order
			- if yes then format to desired order , replace 5 with S or vice versa
			- if not then return None
		- 
- Inference
	- different license plate number for same car in different frame
		- from all the frames of a car id, select the license plate text with highest confidence.
	- missing frame
		- interpolate between frames
	- process the csv file generated in detection to make the inference video.
- Converting annotations from PASCAL to Yolo format
	- get xmin, ymin, xmax, ymax, width, height from the xml file using xml.tree.elementtree
		- et.parse(file)
	- calculate xc, yc, w, h
		- (xc = (xmin+xmax) / 2 ) / width
		- (yc = (ymin+ymax) / 2 ) / height
		- w = (xmax-xmin) / width
		- w = (ymax-ymin) / height
- Yolo
	- original paper by Redmond et. al, uses darknet
- Yolov4
	- Alexey et. al
	- Bag of freebies
	- Bag of Specials
- yolov5
	- Glenn Jocher
	- CSP backbone
	- PA-NET neck
- PP-yolo
	- Xiang Long et. al
 - SORT - Simple Online and Realtime tracking
	 - https://www.linkedin.com/pulse/object-tracking-sort-deepsort-daniel-pleus/
	 - Detection
	 - Kalman Filter
	 - Data Association
		 - calculate IoU
		 - hungarian algorithm
			 - alignment 
		 - creation and deletion of track
			 - when no 


### Recommendation System
- Dataset
	- goodreads 10k dataset
	- Books
	- Users
	- Ratings
- Recommender
	- Popularity based
		- merged ratings and books
		- filtered books which had avg. ratings more than 100
		- select top 50
		- filter using 
			- trusted user, ratings > 200
			- trusted books, ratings > 50
		- make pivot table between user-id and book title with ratings as value
		- find cosine similarity for the pivot table


## Price Prediction
##### Car
- Dataset
	- Car dekho (4340 records)
	- name 
	- year
	- selling price
	- seller type
	- owner
	- transmission
	- fuel
	- km driven
- Preprocessing
	- checked missing values, 0
	- checked duplicates, 700+
	- separated model name from column 
- EDA
	- value count plots
	- selling price vs different column
	- spotting outlier 