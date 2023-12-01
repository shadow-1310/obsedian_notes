tags: 

## Tutorials

### Video capture
#### cv2.VideoCapture()
<code>cap = cv2.VideoCapture()</code>
<code>ret,frame = cap.read()</code>
- it returns ret and frame
	- **ret**, it is return status of the frame True or False
	- **frame** is actual frame captured by the webcam 
- by using cap.get(id), we can get different properties of the frame
	- for example <code>cap.get(3)</code> gives width of the frame
	- cap.get(4) gives height of the frame
- [OpenCV Python Tutorial #3 - Cameras and VideoCapture - YouTube](https://www.youtube.com/watch?v=rKcwcARdg9M)
#### cv2.VideoWriter()
<code>writer = cv2.VideoWriter()</code>
<code>writer.write(frame)</code>
- it can write processed image to a new video file
- input parameters-
	- output file name (eg: output.avi).
	- specify the **FourCC** code
		- <code>cv2.VideoWriter_fourcc(*'XVID')</code>
	- number of frames per second (fps)
	- frame size
- [official documentation](https://opencv24-python-tutorials.readthedocs.io/en/latest/py_tutorials/py_gui/py_video_display/py_video_display.html)


Opening
Closing
Gradient
Black Hat
