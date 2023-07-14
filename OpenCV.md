tags: 

## Tutorials

### Video capture
#### cv2.VideoCapture()
<code>cap = cv2.VideoCapture()</code>
- it returns ret and frame
	- **ret**, it is return status of the frame True or False
	- **frame** is actual frame captured by the webcam 
- by using cap.get(id), we can get different properties of the frame
	- for example <code>cap.get(3)</code> gives width of the frame
	- cap.get(4) gives height of the frame
- [OpenCV Python Tutorial #3 - Cameras and VideoCapture - YouTube](https://www.youtube.com/watch?v=rKcwcARdg9M)