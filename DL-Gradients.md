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
	- because the way computer memory is designed it is faster than taking normal size like 500

### Batch Gradient Descent



## Exponentially Weighted Moving Average
- Advantages over simple moving average
	- we need to keep track of only one variable to calculate average over any time window, so memory efficient
	- computationally also efficient
- disadvantages over simple moving average
	- not accurate
	- latency in trend
- Bias Correction
	- bias term to rectify for initial warming up time.

## Gradient Descent with Momentum
$$V_{dw}={\beta}V_{dw}+(1-{\beta})dw$$
$$V_{db}={\beta}V_{db}+(1-{\beta})db$$
$$W=W-{\alpha}V_{dw}$$
$$b=b-{\alpha}V_{db}$$

where $\beta$ decides how many previous gradient we want to give weightage to, higher $\beta$ means smooth change 

### RMSprop
- here we multiply the square of the current weight while calculating momentum
$$S_{dw}:={\beta}S_{dw}+(1-{\beta})dw^2$$
$$W:=W-{\alpha}\frac{dw}{\sqrt{S_{dw}}}$$