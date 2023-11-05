
### Generative Configuration
- [tutorial](https://www.coursera.org/learn/generative-ai-with-llms/lecture/18SPI/generative-configuration)
#### Greddy Decoding
- choose the word with highest probability

#### Random Sampling
- does random sampling with the probability of the token as weight. it has 2 types
##### top-k sampling
- use only the top k tokens having highest probabilities to consider for random samling
##### top-p sampling
- total cumulative probability to choose from


#### Temperature
- low temperature (<1)
	- strongly peaked probability distribution, prediction will be stable
- high temperature(>1)
	- broader flatter probability distribution
	- higher degree of randomness and creative

