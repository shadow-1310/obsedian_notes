tips - prepare well on the topic of explainable AI
read for interview if selected, 
- [computer vision explainability](https://christophm.github.io/interpretable-ml-book/index.html)
- [collection of ML interpretability](https://github.com/jphall663/awesome-machine-learning-interpretability)
- [yt video on interpretability methods](https://www.youtube.com/watch?v=Yg3q5x7yDeM)
#### Requirements
- NLP
	- Word2vec,
	- NER,
	- topic modeling,
		
	- RNNs/LSTMs,
	- Transformers,
	- BERT
- Computer Vision
	- CNN
	- ResNet
	- MobileNet,
	- Unet,
	- Mask-RCNN,
		- [[CV - Semantic Segmentation]]
		- instance segmentation
			- object detection
			- semantic segmentation
	- Siamese Networks,
	- Grad Cam,
		- way to visualize which regions are contribution more to classification
		- [nptel-theory](https://www.youtube.com/watch?v=VmbBnSv3otc)
		- [theory on grad-cam](https://www.youtube.com/watch?v=Y8mSngdQb9Q)
		- [tutorial on keras](https://www.youtube.com/watch?v=6YZoZ9Vtez0)
		- [keras documentation](https://keras.io/examples/vision/grad_cam/)
		- Cons
			- need to do retrain
	- Image augmentation techniques,
		- vertical axis mirroring
		- random crop
		- rotation
		- shearing 
		- local warping
		- color shifting
		- PCA color augmentation
		- one thread fetch data from storage and other thread pass data to training network
	- GAN
	- Vision Transformers


## Assignment

#### Computer Vision
- The objective of this assignment is to develop a solution using image processing techniques to partially de-annotate an image, given an original image and a fully annotated image

#todo/deadline
- [ ] akaike assignment, 7 Nov'23

[github solution of NLP](https://github.com/ramananstark/internship-assignment-nlp/blob/main/script.py)
[huggingface qna](https://huggingface.co/docs/transformers/tasks/question_answering)
#### NLP
- [good video](https://www.youtube.com/watch?v=tpxl-UnfmQc)
- [leaf question answering repo](https://github.com/KristiyanVachev/Leaf-Question-Generation/tree/main)
- [hugging face](https://huggingface.co/docs/transformers/tasks/multiple_choice)
- [T5 hugging face](https://huggingface.co/docs/transformers/model_doc/t5)

##### Steps
[questgen medium post](https://towardsdatascience.com/practical-ai-automatically-generate-multiple-choice-questions-mcqs-from-any-content-with-bert-2140d53a9bf5)
[questgen website](https://dashboard.questgen.ai/?code=ab5f662f-eef1-4dad-b91a-f93629f4097b)

- Libraries
	- T5 conditional generation, T5 Tokenizer

functions
- generate_questions_mcq
- tokenize_sentences
- get_keywords
[[Akaike-documentation]]
[[Akaike-cv_task]]