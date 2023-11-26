 - don't use a grid like approach like Machine Learning
 - because some hyperparameter is important than others, so we need to try out more values of them
 - Coarse to Fine approach
	 - first find which values works best in the samples
	 - then choose points nearer to those samples

##### sample using logarithmic scale
- learning rate
	- While searching for learning rate between 0.0001 and 1, use log scale
- parameter $\beta_1$ for exponentially weighted average
	- sample for $1-\beta_1$
 