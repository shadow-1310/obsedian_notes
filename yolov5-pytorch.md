tags : #yolo

## Steps for custom training
### requirements
#### image and annotations
- image files with their corresponding annotation in .txt files in the same directory.
- Note: image having no objects need not have .txt file like below
	- ![[Pasted image 20230715222942.png]]
#### data.yaml file
- this file will contain about the directories of training and validation file along with the classes. A sample is shown below
	- ![[Pasted image 20230715223235.png]]
## training parameters
- [Load YOLOv5 from PyTorch Hub ⭐ · Issue #36 · ultralytics/yolov5](https://github.com/ultralytics/yolov5/issues/36)
## Files generated after training
- best.pt file
	- best.pt is the checkpoint file that has the best validation loss during training. More details [here](https://github.com/ultralytics/yolov5/issues/8701)


## flags for detect.py

![[Pasted image 20230715222514.png]]
