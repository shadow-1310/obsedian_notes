### PYQ questions
- [NPTEL ML assignments](https://www.youtube.com/playlist?list=PL__28a0xFM-8gW3v63c3NzjsPlrBRp3WX)
	- Week 1: done
	- Week 2: done
		- ID3, decision tree
		- calculate entropy, decision tree
		- why not multiway split in DT instead of binary split
		- ![[Pasted image 20230919112453.png]]
		- ![[Pasted image 20230919112934.png]]
	- Week 3
		- KNN
		- PCA
		- recommendation system
		- LDA
		- Pearson corelation
	- Week 4
		- Bayes Theorem problems. spam/not spam
		- Naive Bayes assumption
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