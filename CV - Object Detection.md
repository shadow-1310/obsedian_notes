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
- Loss function modifications
	- w/o modification it will weight localization error and class prediction error same
- train vector