## Definition
- Policy
	- Mapping between state space and policy space
- Value function
	- Reward accumulated starting from the state under a policy
- Transition Probability
	- probability of moving between state under an action.
- Random Variable
	- Discrete random variable - PMF
	- Continuous Random Variable - PDF

## DTMC
- State change occur only on discrete time
- $P(X_{n+1}=j|X_n=i,X_{n-1}=i_{n-1},...,X_0=i_0)=P(X_{n+1}=j|X_n=i)$
- Markovian Property
	- Conditional distribution of any future state given present and past state depends only on present state.
- Stationary Property
	- Transition probability is independent of time
- For a finite state 
- Condition for existence of limiting distribution
	- Aperiodicity
		- all states are aperiodic
	- Irreducibility
		- if all states communicate with each other
## CTMC
- State change can occur at any time
### Poisson 
- Exponential distribution
- ![[Pasted image 20240223214213.png]]
- independent increment
- stationary increment

DTMC vs CTMC
- past doesnot matter
- transition probability doesnot depend on time
- for CTMC event can occur at any time
- for DTMC events occur at distinct time.

CTMC View

### MDP
#### Types of Policies
- Markovian Policy
	- Depends only on the current state
- Stationary Policy
	- Identical Markovian Policy at every epoch


## Value Iteration Algorithm
- Resources
	- [medium blog with code](https://medium.com/@**ngao7**/markov-decision-process-value-iteration-2d161d50a6ff#807e)
	- [opengenus 1D example](https://iq.opengenus.org/value-iteration-algorithm/)
	- 

## Policy Iteration 
- Resources
	- [medium blog with code](https://medium.com/@ngao7/markov-decision-process-policy-iteration-42d35ee87c82)

### Example problems
##### Gambler's ruin
###### Server replacement problem

#### Threshold Policy
- continue if i < i*, replace if i >= i*


## MAB
- Stochastic MAB
	-  IID
	- Markovian
		- Rested
			- States of arm not played -> frozen
		- Restless
			- States of arm not played -> may change
- Regret
- Suboptimality gap of an arm
	- Regret Decomposition Lemma
- Bandit Algorithms
	- Greedy
		- Maintain estimate (sample average) for each arm
		- Linear regret
	- epsilon-greedy
		- with epsilon probability locks into suboptimal arm
		- linear regret
	- epsilon_t-greedy
		- decaying exploration
		- design mechanism with 
		- sublinear (logarithmic) regret
	- UCB - uses Hoeffding bound
		- doesnot depend knowledge of sub-optimality gap
		- logarithmic regret
		- upper confidence bound overestimates the unknown mean
	- KL-UCB - uses Chernoff bound
		- asymptotically optimal
		- tighter bound than Hoeffding bound

Lower Bound
- If all arms are similar -> high regret
- If arms are very different -> low regret
- 2 metrices to signify
	- Suboptimatility gap 
	- KL distance between arms


#### Thomson Sampling
