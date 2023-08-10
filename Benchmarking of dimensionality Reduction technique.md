[[2023-08-07]]
**Done -** 
- training the models with cross validation without using any dimensionality reduction (i.e on 5043 components)
**To-do**
- Read papers about how they have described affect of reduced components on the visualization of the image.
	- [(PDF) Analysis of Medical Data Using Dimensionality Reduction Techniques](https://www.researchgate.net/publication/268279845_Analysis_of_Medical_Data_Using_Dimensionality_Reduction_Techniques)
	- [A fast approach for dimensionality reduction with image data - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S003132030500169X)
	- [Distance based kernel PCA image reconstruction | IEEE Conference Publication | IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/1334618)
	- [Efficient registration of pathological images: A joint PCA/image-reconstruction approach | IEEE Conference Publication | IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/7950456)
	- [Object detection using image reconstruction with PCA - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0262885607000820) ^d5d20a

[[2023-08-08]]
To-do ^64f549
[[2023-08-10]]
To-do
- generate supplement plots for t-SNE, FA with different parameter value
### Find papers to justify methodology procedure - 
- conversion of image matrix to array
	- [comparison of ML vs DL](https://iopscience.iop.org/article/10.1088/1742-6596/1314/1/012148/pdf)
		- ![[Pasted image 20230809215316.png]]
	- [Frontiers | Image-Based Cardiac Diagnosis With Machine Learning: A Review](https://www.frontiersin.org/articles/10.3389/fcvm.2020.00001/full?&utm_source=Email_to_authors_&utm_medium=Email&utm_content=T1_11.5e1_author&utm_campaign=Email_publication&field=&journalName=Frontiers_in_Cardiovascular_Medicine&id=509311)
		- ![[Pasted image 20230809220546.png]]
	- [feature extraction and then feed to model](https://www.idosi.org/mejsr/mejsr23(9)15/17.pdf)
		- ![[Pasted image 20230809221646.png]]
	- [Brain Tumor Detection and Classification Using Convolutional Neural Network and Deep Neural Network | IEEE Conference Publication | IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9132874)
		- ![[img-to-array.gif]]
- reconstruction of the images - 
	- [paper having reconstruction formula](https://opg.optica.org/josaa/fulltext.cfm?uri=josaa-4-3-519&id=2689)
		- ![[Pasted image 20230810164028.png]]
	- [stack-exchange explaining image reconstruction](https://stats.stackexchange.com/questions/229092/how-to-reverse-pca-and-reconstruct-original-variables-from-several-principal-com)
		- ![[Pasted image 20230810164204.png]]
- crossvalidation with PCA reference
	- [Paper using PCA separately with train and test data](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/11252/1125217/Incorporating-machine-learning-with-Raman-spectroscopy-to-differentiate-bone-types/10.1117/12.2546463.full?SSO=1)
		- ![[Pasted image 20230808165441.png]]
	- [Paper using PCA with SVM, decision tree to predict heart disease](https://www.researchgate.net/profile/Neeta_Singh2/publication/301335834_Analysis_of_Supervised_Machine_Learning_Algorithms_for_Heart_Disease_Prediction_with_Reduced_Number_of_Attributes_using_Principal_Component_Analysis/links/583d2af708ae502a85e53634/Analysis-of-Supervised-Machine-Learning-Algorithms-for-Heart-Disease-Prediction-with-Reduced-Number-of-Attributes-using-Principal-Component-Analysis.pdf)
		- ![[Pasted image 20230809165327.png]]
	- [Paper using 3 config of data(60-40, 80-20, 90-10)](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9137850)
		- ![[Pasted image 20230809170640.png]]
	- [paper using k-fold Cross Validation with PCA- (Indian authors)](https://ieeexplore.ieee.org/abstract/document/9076533)
		- ![[Pasted image 20230809171855.png]]
		- ![[Pasted image 20230809172035.png]]
		- this paper also uses boxplot for model comparison
			- ![[Pasted image 20230809172754.png]]
		- they are also using mean and SD for model comparison 
			- ![[Pasted image 20230809173526.png]]
- interesting papers found
	- [PCA vs SVD](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7960038)