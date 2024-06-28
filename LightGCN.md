#### Modifications
- removes ReLU non linearity
	- normalized adjacency matrix doesnot include self loop like in the GCN paper
	- combines weight matrix of each layer into a single matrix
	- iteratively diffuse embedding matrix E using $\tilde{A}$
- Multi-step diffusion
	- $A^k$ never gets materialized because it is a dense matrix
- Final embedding is avg of embedding from all layer