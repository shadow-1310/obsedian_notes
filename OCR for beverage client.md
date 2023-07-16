tags: #projects/ocr #unfinished #poc
people involved : [[Amit Sir]] , [[Pushpendra]], [[Bhargav-internmate]]

## Problem Statement
---
- we have photos of bottle with with their label
- we need to extract some important fields like MRP, MFG, expiry date, batch no., quantity etc.
- sample photo ![[11_4723879.jpg]] 

## Approach-1
---
### basic idea
- briefly write about this approach.....
### Tasks

#### Task 1
- Details
	- we have a veg/non-veg symbol on the label, so we will take it as a template and do template matching with opencv.
	- next based on the location of the template, we will extract the actual white section of the label.
- provide code link here

#### Task 2
- Step 1 - placing the images in respective directory - with code ^8b4ea2
	- we have 48 original images place each image in their own directory
	- provide code link here
- Step 2- Crop the images into small sections - took total approx. **4-5 hours** ^a6513d
	- we have 5 fields in an image, MRP, mfg, use_by, batch and qty. Crop each field and place it in the same folder.
- Step 3- preprocess the image and place them in separate directory ^4570bb
- step 4- inference the processed images with EasyOCR
	- **plan-change** - inference the original images, not the processed ones. ^429ee9
- step 5 - annotate the images using [[labelImg]] and then yolov5 model. Following are the results
	- ![[Screenshot from 2023-07-16 01-22-00.png]]
	- ![[val_batch0_pred.jpg]]
	- ![[val_batch1_pred.jpg]]

## Things Learned
--- 
- write the new things learned

## Problems faced
--- 
- what are the problems we faced
