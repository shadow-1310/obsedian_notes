## Learning resource
- [AI-epiphany blog](https://gordicaleksa.medium.com/how-to-get-started-with-graph-machine-learning-afa53f6f963ajjk)
- https://gnn.seas.upenn.edu/lectures/lecture-3/

## Why do we need GNN
Graph data is different in following senses
- Size and shape
	- FFNN takes same size input ,but graph size may vary and we cannot simply remove nodes to make it same size
- Isomosrphism
	- permutation invariance
- Grid Structure
	- Graphs are in non euclidean space 
## Applications
- Node level predictions
	- does this person smoke
- Edge level prediction
	- next netflix video
- graph level predictions
	- is this molecule a suitable drug
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
Degree of a node
- degree $d_i$ of node i is the sum of the weights of its incident edges
Degree Matrix
- It is a diagonal matrix D with degrees as diagonal entries
Laplacian Matrix of a graph
- Laplacian matrix of a graph with adjacency matrix A is, L = D - A
Normalized adjacency matrix
- expresses weights relative to nodes' degrees
- pre and post multiplication by degree matrix
- $\bar{A}=D^\frac{-1}{2}AD^\frac{-1}{2}$
Graph Shift Operator S
- It is a stand in for any matrix representation of the graph
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