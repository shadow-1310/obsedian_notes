## problem statement

we have a drone hovering over crop field, we need to process that video and find the sapling count.

approach 1
- use opencv contour detection to colour match the saplings and find contour of them. Which can be used for counting purpose

approach 2 
- annotate the images for the sapling and train a yolo model.

## problems faced
---
- there was overlap between the images when the drone returns and follows an almost parellel path.

#### solution
- we will find (latitude, longitude) for all the corner points of an image. (we have (lat, lon) for the centre point). 
- Let's assume we have some yaw in our camera, pitch and roll to be zero for the time being.
- the drone provides exif data which have the following. [DJI Tags](https://exiftool.org/TagNames/DJI.html)
	- ![[Pasted image 20230809001652.png]]
	- here we can see camera pitch, yaw and roll is given. 
- refrences - [python - Get lat/long given current point, distance and bearing - Stack Overflow](https://stackoverflow.com/questions/7222382/get-lat-long-given-current-point-distance-and-bearing)
	- ![[Screenshot from 2023-08-09 00-09-56.png]]