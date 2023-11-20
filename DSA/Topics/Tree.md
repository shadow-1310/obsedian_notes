tags: #dsa/tree #unfinished 
## Basic Overview
- preorder 
	- root at first 
- post order
	- root at last
- inorder
	- root at centre

### Implementation from scratch
#### pseudo-code

#### code
[[Segment tree with Lazy algo]]

## Related Problems
---
- [x] [[226-Invert Binary Tree]] last done: [[2023-10-04]]
- [x] [[98-validate binary search tree]] last done [[2023-10-04]]
- [x] [[94-Binary Tree Inorder traversal]] last done: [[2023-10-04]]
- [x] [[144-Binary tree preorder traversal]] last done [[2023-10-04]]
- [x] [[145-Binary Tree Postorder traversal]] last done [[2023-10-04]]
- [x] [[110-Balanced Binary Tree]] last done: [[2023-10-04]], revise more not that easy
- [x] [[100-Same Tree]] last done: [[2023-10-04]]
- [x] [[101-Symmetric Tree]] last done: [[2023-10-04]]
- [x] [[102-Binary Tree level order traversal]] last done: [[2023-10-04]]
- [x] [[103-Binary Tree Zigzag level order traversal]] last done: [[2023-10-04]] give attention
- [x] [[104-Max depth of binary tree]] last done: [[2023-10-04]]
- [x] [[105-Construct Binary Tree from preorder and inorder]] last done: [[2023-10-04]], attention
- [x] [[108-converted sorted arry to bst]] last done: [[2023-10-04]]
- [x] [[1448-Counting Good Nodes in Binary Tree]] last done: [[2023-10-04]]
- [x] [[543-Diameter of Binary Tree]], last done: [[2023-10-23]]
- [x] [[114-Flatten Binary Tree to linked List]], last done: [[2023-10-24]], very tricky
- [x] [[112-Path Sum]], last done: [[2023-10-24]]
- [x] [[113-Path Sum II]], last done: [[2023-10-24]]
- [x] [[437-Path Sum-III]], last done: [[2023-10-24]], very very tricky
- [x] [[654-Maximum Binary Tree]], last done: [[2023-11-20]]
- [ ] 
#### Segment tree
[build tree](https://www.youtube.com/watch?v=-dUiRtJ8ot0)
[point and range update in lazy propagation a](https://www.youtube.com/watch?v=rwXVCELcrqU)
- whenever you visit a node, update its lazy work to 0 while propagating to child nodes
- [[307-Range Sum Query]]