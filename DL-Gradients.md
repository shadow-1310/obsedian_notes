#### Gradient Checking
- it is a way of checking if the gradient checking algorithm is implemented correctly bu cross varifying with a numerical method
- [stanford blog](http://ufldl.stanford.edu/tutorial/supervised/DebuggingGradientChecking/)
- don't forget to add regularization term in cost function while calculating approximate gradients
- it doesn't work with dropout
- run grad check at initialization, then again run after some training when weight values are far from 0, 
	- because sometimes gradient calculation works well when gradients are near 0 which is the case in initialization



## Gradient Descent Types

### Stochastic Gradient Descent
### Mini-batch gradient descent
- choose batch size in power of 2 like 64, 128,256, 512 etc.
	- because the way computer memory is designed it is faster than taking normal size like 500,1000

### Batch Gradient Descent


