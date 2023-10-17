## Topics

### Other IIT questions
- pandas merge, concat, join, combine methods
	- pd.merge / df.merge
		- on
		- how
	- pd.concat
		- stitches row-wise by default
		- objs
		- axis
		- join - inner/outer, defaut -> outer
	- df.join
		- on -> column name
		- how - left, right, inner
	- df.combine - Perform column-wise combine with another DataFrame.
		- takes a lambda function to combine columns of the dataframes
- generators
- gini coefficient and entropy calculation of a dataset
	- gini $$GI = 1-p_1^2-p_2^2-...$$
	- entropy $$H(s) = -p_+log(p_-)-p_+log(p_+)$$
- find MLE of mean and variance
	- [Bessel's correction](https://www.statisticshowto.com/bessels-correction/)
- statistical test
### Round1 - Maths & Stats(33.33%) - 30 mins
- [ ] Probability
	- [MCQs](https://www.analyticsvidhya.com/blog/2017/04/40-questions-on-probability-for-all-aspiring-data-scientists/)
- [ ] Probability Distributions
- [ ] Sampling
- [ ] Correlations
- [ ] Hypothesis testing
- [ ] Statistical significance
- [ ] CLT
- [ ] Paired Means Tests
- [ ] Baye's Theorem
- [ ] Linear Algebra
	- [x] EigenValue Decomposition - [ritvikmath](https://www.youtube.com/watch?v=KTKAp9Q3yWg)
		- only applies to diagonal square matrix
		- eigenvector and eigenmatrix, $$Ax = \lambda x$$ 
		- usefull to reduce coputational cost of matrix power.
		- if we do matrix A to the power p, we need at least Log2(p) operations. while using eigen decomposition, we need only 2 matrix operations.
		- $$A^p = U\Lambda^pU^{-1}$$
		-  where A -> matrix, U -> eigenvector, lambda->eigenvalue
	- [ ] SVD - [ritvikmath](https://www.youtube.com/watch?v=HAJey9-Q8js)
		- it is useful for compression of big matrices, we can express a Matrix by the following.
		- $$M = U*\sigma *V^T, \newline $$
		- where 
			- M -> m * n
			- U, orthonormal matrix -> m * p
			- sigma, diagonal matrix -> p * p
			- V^T , orthonormal matrix-> p * n
		- right singular vectors, V
		- left singular vectors, U
		- singular values, sigma1, sigma2, sigmap
	 - [ ] Matrix Operations
		 - [ ] rank of a matrix
			 - if a matrix has rank p, it can be expressed as sum of p number of rank 1 matrices(atom matrices).
		 - [ ] jacobian
			 -  
		 - [ ] finding eigenvector and eigenvalue, [ritvik-tutorial](https://www.youtube.com/watch?v=glaiP222JWA)
		 - $$if\;det(A) = 0, A\;is\;not\;invertible$$
		$$det(A-\lambda*I)=0,\newline because\;(A-\lambda*I)*x=0, which\; gives (A-\lambda*I) as\;non determinant$$
		 - [ ] Matrix Norms -[ritvik](https://www.youtube.com/watch?v=DkyM93Wgh_0)
			 - $$||AB||_p \leq ||A||_p ||B||_p$$
			 - $$||A^k|| \geq Max|\lambda _i|^k$$
		 - [ ] singular values vs eigen values
### Round2 - Classical ML and DL(66.67%) - 45 mins
- [ ] Bagging 
- [ ] Boosting
- [ ] Gradient Descent
- [ ] Decision Trees
- [ ] Linear and Logistic Regressions
- [ ] Random Forest
- [ ] Gradient Boosting Machines
- [ ] XGBoost
- [ ] LiteGBM
- [x] SVM and kernel trick
- [ ] Regularization
- [x] Bias-Variance trade off
- [ ] Evaluation Metrics (precision, recall, f1, fpr etc.)
- [ ] confusion matrix
- [ ] missing data imputation
- [ ] matrix factorization
- [ ] density estimation (KDE, K-Means)
- [ ] MAP
- [ ] MLE
- [ ] NLP basics
- [ ] TF-IDF
- [ ] Embedding based approach ( Word2Vec, FastText, BERT)
- [ ] LSTM, CNN, RNN, transformers, GANs

### Round3 - Programming Skills
- part 1- Data handling
- part 2- ML basics

### Round4 - Case study