## Learning resource
- [AI-epiphany blog](https://gordicaleksa.medium.com/how-to-get-started-with-graph-machine-learning-afa53f6f963ajjk)
## Intro
Graph is defined by
- vertices V
- Edges E
- adjacency matrix A

Graph features
- Node features
	- atom type
- edge features
	- bond type
- graph features
	- molecular energy
## Types
- Spectral
	- computationally expensive
	- inherently expensive
- Spatial
	- message passing

## What GNN do
- They create rich representation of each node using their neighbour information. We can use this new latent representation for various tasks as below
![[Pasted image 20240613135931.png]]

## Assumptions in ConvNets
- Local (Hubel-Wiesel, 1962)
- Stationary (shared patterns)
- Hierarchical (multiscale)
	- combination of low-level features make the high level features in images

## GCN
- template matching for graphs
	- no node ordering
	- heterogeneous neighbourhood
- convolution theorem for graph
	- time complexity is $O(N^2)$ for normal fourier transform
	- it reduces to $O(N)$ only for grid like data(e.g. image)

Spectral Graph Theory 
- Core operator is Normalized Laplacian
	- interpretation is measure of smoothness
- Eigen decomposition of Laplacian Graph
	- fourier functions -> laplacian eigen vectors