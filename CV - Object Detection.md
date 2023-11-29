### Non-max suppression
- parameters
	- prob threshold
		- discard all bboxes which has less probability than this threshold
	- IoU threshold
		- remove all bboxes which has more IoU than current preedicted bbox
- Steps
	- discard all bboxes which has less probability than this threshold
	- select the bbox with highest prob as current prediction
	- remove all bboxes which has more IoU than current preedicted bbox.
	- again repeat for finding the bbox with highest prob
- NMS is carried out separately for each of the class.


### YOLO
[medium blog](https://medium.com/analytics-vidhya/yolo-explained-5b6f4564f31)
- Architecture
	- backbone, neck and head
		- backbone is CNN model which can capture minute details
		- neck is predicting probabilities for bbxoes.
		- head 
			- it is 7x7x30 in the original paper
- Loss function problems
	- w/o modification it will weight localization error and class prediction error same.
	- giving same weightage to small and big bounding box error
		- actual ->100 and predicted -> 98, have loss of 2
		- actual -> 10 and predicted -> 8 has also loss of same 2, but this one should be more loss compared to above one
		- $w_i$
- train vector
	- S x S x (C + B * 5)
		- SxS grids
		- C -> number of classes
		- B -> no. of bboxes per grid
		- 5 -> (x, y, w, h, confidence)

#### Limitations
- This is a limitation of the YOLO algorithm itself, and if there are multiple objects of different classes in one grid cell, the algorithm will fail to classify both correctly. 