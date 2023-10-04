topic: #dsa/tree [[Tree]]

### basic info
- source:  
- serial no: #leetcode/94
- first_done: [[2023-06-13]]
	- first_revised: [[2023-07-30]]
- last_revised: [[2023-10-04]]
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/binary-tree-inorder-traversal/description/?envType=featured-list&envId=top-interview-questions
- solution_link: https://www.youtube.com/watch?v=g_S5WuasWUE

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- use a empty list to store the values.
- use a helper dfs function which take one argument, the node
- base case is if given node is None return
- otherwise first call dfs(node.left)
- then append current node value
- after that dfs(node.right)

#### mistakes
- don't forget to return the res

#### code snippet
```python

```