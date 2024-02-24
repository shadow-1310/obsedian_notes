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