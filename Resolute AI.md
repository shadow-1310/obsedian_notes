### peoples
- [[Amit Sir]]
- [[Abhijit Sir]]
- [[Pushpendra]]

- started learning [[YOLO]] first here
- started learning [[OpenCV]] first here
## Learnings
---
##### Self-learning tasks
- yolov4
	- setup yolov4 on local
	- object detection on video
- yolov5
	- setup yolov5 on local
	- object detection
- how to use labelImg and bulk image downloader OIDv4 toolkit
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
					- detecting the horizontal lines using horizontal kernel
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


