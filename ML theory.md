#### github repo
- https://github.com/youssefHosni/Practical-Machine-Learning
## MCQ
- https://www.analyticsvidhya.com/blog/category/skilltest/
## Topics

### Maths & Stats
- Probability
- Probability Distributions
- Sampling
- Correlations
- Hypothesis testing
- Statistical significance
- CLT
- [[ML-Statistical Tests]]
- Paired Means Tests
- Baye's Theorem
- Linear Algebra
	- SVD
	- EigenValue Decomposition
	- Matrix Operations

### Classical ML and DL
- Bagging 
- Boosting
- Gradient Descent
- Decision Trees
- Linear and Logistic Regressions
- Tree Based Models
	- [MCQs1](https://www.analyticsvidhya.com/blog/2017/09/30-questions-test-tree-based-models/)
	- [MCQs2](https://www.analyticsvidhya.com/blog/2016/12/detailed-solutions-for-skilltest-tree-based-algorithms/)
	- Random Forest
	- Gradient Boosting Machines
	- XGBoost
	- LiteGBM
		- histogram / bin way of splitting nodes in DT
		- Exclusive Feature Bundling
		- GBOSS (Gradient Based One Side Sampling)
			- sampling is done from the records where error is low, the records where error / gradient is high, they will be taken as a whole
	- Adaboost
		- uses decision stump as weak learners
- SVM and kernel trick
- Regularization
- Bias-Variance trade off
- Evaluation Metrics (precision, recall, f1, fpr etc.)
- confusion matrix
- missing data imputation
- matrix factorization
- density estimation (KDE, K-Means)
- MAP
- MLE
- NLP basics
- TF-IDF
- Embedding based approach ( Word2Vec, FastText, BERT)
- LSTM, CNN, RNN, transformers, GANs
### PYQ questions
---
#### [NPTEL ML assignments](https://www.youtube.com/playlist?list=PL__28a0xFM-8gW3v63c3NzjsPlrBRp3WX)
- **Week 1**: done
- **Week 2**: done
	- ID3, decision tree
	- calculate entropy, decision tree
	- why not multiway split in DT instead of binary split
	- ![[Pasted image 20230919112453.png]]
	- ![[Pasted image 20230919112934.png]]
- **Week 3**
	- KNN
	- PCA
	- recommendation system
	- LDA
	- Pearson corelation
- **Week 4**
	- Bayes Theorem problems. spam/not spam
	- Naive Bayes assumption
	- Bayesian Belief Network problems (practice the numericals)
		- [youtube tutorial](https://www.youtube.com/watch?v=hEZjPZ-Ze0A)
	- Markov Blanket
- **Week 5**
	- SVM decision boundary, 
	- kernel function- also a similarity function
	- when soft margin is preferred - noisy and overlapping data
	- SVM parameters - [youtube video](https://www.youtube.com/watch?v=fqhHBCfNy6s)
		- gamma - effects only when kernel is non linear
			- low gamma - large similarity radius, more points are grouped together
			- high gamma- small similarity radius, less points are grouped together
		- C -  slack variable (cost parameter)
			- trade off between misclassification and the margin.
			- adds penalty for each misclassified point
			- so high C means hard/smaller margin, chance of overfitting 
			- low C means soft/ larger margin
- **Week 6**:skipped for now
	- Neural Networks
- **Week 7**
	- Concept learning - Find-S or Candidate Elimination
		- [youtube video](https://www.youtube.com/watch?v=z5AKsT3apWI)
		- General Hypothesis
			- most general, {?, ?, ?, ?, ?}
				- ? means any value is acceptable
		- Specific hypothesis
			- most specific, {phi, phi, phi, phi, phi}
				- phi means no value is accepted
	
		- Instance space (doesn't include ?, phi),
			- f1 * f2
		- hypothesis space (includes ? and phi)
			- (f1+2) * (f2+2)
		- semantically distinct hypothesis (have phi only one time)
			- (f1+1) * (f2+1) + 1
	- Find-S algorithm (considers only +ve examples)
		- [edureka video](https://www.youtube.com/watch?v=ncOirIPHTOw)
	- questions on 
		- VC dimension - Vapnik Chevronenkis Dimension (haven't learned yet)
		- PAC learning
	- questions on ensemble techniques
		- Taking decision from multiple classifier
		- why bagging is done- 
			- impact on bias and variance
			- it is similar to dropout in neural network
	- questions on boosting techniques
		- which datapoints are given more weight
			- those were misclassified in previous learner
		- how adaboost is trained
			- how final prediction is made
				- weighting the prediction of weak learners based on their accuracy
		- adaboost ensemble classifier
- **Week 8**
	- K-Means Clustering
		- iteration step for calculating new centroid
		- calculate distance between points with different metric
			- euclidean
			- manhattan etc
	- computational cost comparison in , Q9 recheck
		- Kmeans
		- single linkage
		- complete linkage
	- when K-means fails
		- non convex data points
		- outliers
		- different distribution
	- expectation maximization clustering algorithm, K-Means
		- suffers from problem of convergence at local minima
	- Quality of clustering
		- internal evaluation
			- Davies Boulding Index
		- external evaluation
			- Rand Index
			- Jaccard index
			- f measure



## Specific ML models
---
## Linear Regression
[medium article](https://ai.plainenglish.io/the-normal-equation-for-linear-regression-25fddea63899)
- Normal Equation
	- $$theta = (X^TX)^{-1}(X^Ty)$$
	- find dimension of different parameters, theta, X, y
	- Read about projection and projection metric later
#### Tricky questions
- Why is there a 2 at the denominator of the mean squared error function?
	- [answer](https://datascience.stackexchange.com/questions/29526/why-is-there-a-2-at-the-denominator-of-the-mean-squared-error-function)
#### SSE, SSR, SST, coefficient of determination(R2)
$$SST = SSR+SSE$$
$$R2 = \dfrac{SSR}{SST}$$
- https://www.youtube.com/watch?v=aq8VU5KLmkY
	- explained deviation (we get SSR), 
	- unexplained deviation(we get SSE)

### Logistic Regression
#### Maximum Likelihood
[ritvikmath](https://www.youtube.com/watch?v=VOIhswqFWVc&t=1s)
- given all the features and weights, we want to maximize the probability that the dataset exists.
- we take Log of the likelihood because of computation reasons, as multiplication of all the probabilities is going to be a very small number.
- MLE - parameter vector(beta vector) which maximizes the likelihood function
- no closed form solution to maximize the the function, we can't use methods like normal equation similar to Linear regression
- but we can use Gradient Ascent to maximize the function

#### Likelihood Ratio Test
[TDS blog](https://towardsdatascience.com/the-likelihood-ratio-test-463455b34de9)
- it is used to compare 2 models on the same data
- to use LR test, the 2 models must be nested
	- nested models are models that can be obtained by restricting a parameter in a more complex model to be 0.
	- [stack exchange question](https://stats.stackexchange.com/questions/455708/what-defines-nested-model-for-the-likelihood-ratio-test)
### Decision Tree
- learn to calculate entropy from a data table (asked in NPTEL)


### Time-series
- Ratio to trend method
	- used for finding seasonal variations.

### Markov Chain
- [youtube ritvikmath](https://www.youtube.com/watch?v=prZMpThbU3E)
- 