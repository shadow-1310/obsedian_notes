## GAN
- Discriminator - It is a classification model
- Generator - generates samples
- Motive
	- we have samples from distribution D but we don't know the distribution
	- we want to generate distribution D' which is close to D.
- How it works theoritically
	- Z is a random distribution with sample set z where $z\epsilon{Z}$
		- Z is some random noise, can be thought of latent representation of the image.
	- we use generator G to produce sample G(z) also called generative sample with distribution D', $G(z)\sim D'$
	- such that it closely resembles D with some mathematical parameter like L1 or L2 norm.
- Value Function
	- [watch this nptel video at 12:00](https://www.youtube.com/watch?v=1ju4qmdtRdY)
	- this is the function that the discriminator tries to maximize using Gradient Ascent and generator tries to minimize using gradient descent.
	- we put the expectation, E term because we are doing it for the whole dataset, log term is only for one datapoint
	- we replace the summation by E term because it is a continuous distribution 
- K-value
	- for every k updates of discriminator we update the generator once.

#### Pros of GAN
- robust to overfitting as it never sees the training data
- sampling is straightforward
- training doesn't involve MLE.

#### Cons of GAN
- probability distribution is implicit
	- not straightforward to compute P(x)
	- Vanilla GANs are good for sample distribution only
- training is hard
	- non convergence
	- mode collapse
- SGD was not designed to find Nash equilibrium.

### DCGAN
- replace FC hidden layer Convolution layers
- use batch normalization after each layer.
- generator
	- use fractional stride convolution
	- use ReLU for hidden layers
	- use tanh for output layer


## Autoencoder for image representation
- Given an original input encoder constructs the hidden representation of the input.
- decoder tries to reconstruct from this hidden representation taking as an input.

## VAE
- [watch this video at 24:00 for the loss function](https://www.youtube.com/watch?v=oJu649cDGyo)
![[Pasted image 20231124122649.png]]
### motive
- finding a distribution $q_{\phi}(z|x)$ of some latent variable which we can sample from $z\sim q_{\phi}(z|x)$ to generate new samples $\tilde{x}\sim p_{\theta}(x|z)$
- Encoder
	- learn a distribution using a neural network, gives parameter of the latent variable distribution z , when we give input x
- sample
	- we need to sample z from that distribution
- Decoder
	- it again tries to reconstruct the X given the latent variable z
- Difference with Autoencoder
	- in autoencoder, it always give same Z, when we give input X
	- but in VAE, z is not deterministic, it is sampled from a latent space distribution

#### Loss Function
- Maximize the log likelihood of minimize the -ve of log likelihood of $logP_{\phi}(x_i|z)$
- minimizing the KL divergence between $Q_{\theta}(z|x_i)$ with P(z) which is standard normal distribution i.e variance is 1
- Assumptions
	- latent variable distribution is as close to the normal distribution.

##### Keywords
- Latent Variable
	- variables which affect our image but we don't see them directly, like image is clear sky, gray sky night sky, these decisions are based on the latent variable
	- [nptel lecture](https://www.youtube.com/watch?v=lXrFX3vjtjQ)

#### Questions
- why we assume only normal distribution for the encoder
	- we take samples from normal distribution then we can map it with a complex function which can mimic any other distribution
- Intractable problem
	- http://www.cs.ucc.ie/%7Edgb/courses/toc/handout29.pdf
#### Problems
- Approximate inference
	- finding the latent variable representation is hard
	- Computing the following is computationally hard as $P(x)$ is not in closed form $$P(z|x) = \frac{P(x|z) \cdot P(z)}{P(x)}$$

#### Solution
- Variational inference - that is why these are called Variational AutoEncoder
	- approximate P(z|x) by another distribution Q(z|x) to be as close as true distribution
	- we converted the problem to problem to an optimization problem where loss function is 
	- $$L = minimize \text{KL}(Q_{\theta}(z|x)||P(z|x))$$
	- we maximize lower bound of P(x) which is called Evidence Lower Bound(ELBO)