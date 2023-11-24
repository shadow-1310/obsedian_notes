#### ZSL Setting
transductive models
- class inductive, instance inductive
	- $D^{tr}, T^{s}$
- class transductive, instance inductive
	- $D^{tr}, T^{s}, T^u$
- class transductive, instance transductive
	- $D^{tr}, T^{s}, T^u, X^{te}$

#### Challenges 
- Hubness problem
	- Both input and semantic features exist in a high-dimensional space, and projecting this high-dimensional vector into a low-dimensional space can lead to clustering of points as hubs due to reduced variance.
- Domain Shift problem
- Bias Problem
- Cross domain knowledge transfer problem


#### Applications
- Zero shot localization by free text
- Retrieving images from text
- Retrieving video events from description
- Robotic Vision

### Learning Methods
- Classifier based methods'
	- Correspondence method
	- relationship method
	- combination method
- Instance based methods
	- projection method
	- instance borrowing methods
	- synthesizing methods