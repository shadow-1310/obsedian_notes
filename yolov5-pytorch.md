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
### flags for detect.py

![[Pasted image 20230715222514.png]]