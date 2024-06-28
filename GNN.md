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

Key properties
- Permutation invariance
	- order or permutation of the nodes should not matter when applying a function
- Permuation equivariance
	- the permutation that we apply to the input graph should result in the exact same permutation also in the output.
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

Graph Representations
- Adjacency matrix
- COO format(edge index)
	- stores 3 list
		- first list is x coordinate
		- 2nd list is y coordinate
		- 3 rd is value at the point 
- Interaction Matrix (for Bipartite graph)
	- since we have 2 types of nodes(U and V)
	- row index represents node type U
	- col index represents node type V

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

## GCN - motivated by spectral methods
but it is not a spectral 
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

Steps
- Transform
	- use a MLP layer to enhance the node features 
- Aggregation
	- aggregate the neighbour node features using a function which is permutation invariant
- Update
	- Combine neighbour features with self feature to update each node's feature

Graph level predictions
- Naive global pooling
	- gets naive features like mean, max, min for the whole graph and concatenate them into a vector
- Hierarchical Pooling
	- Differentiable Pooling
	- TopK Pooling
	- Super/ dummy node
- 

## Rec System
### Resources
- [AI alchemy video](https://www.youtube.com/watch?v=h1zxhx815Fk)
- 
#### Types
Supervised Learning
- labels come from external sources
- predicts ratings of an interaction
Semi-supervised learning
- signals come from graph itself
- link prediction, predict if 2 nodes are connected
- Loss function used is BPR - Bayesian Personalized Ranking
	- 