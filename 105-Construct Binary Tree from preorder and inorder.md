topic: #dsa/tree [[Tree]]

### basic info
- source: #leetcode 
- serial no: #leetcode/105
- first_done: [[2023-06-20]]
- last_revised: [[2023-08-05]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/
- solution_link: https://www.youtube.com/watch?v=ihj4IQGZ2zc

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- 0th index of preorder will give current node
- the n find position of this current node val in inorder
	- this position will split the values for left and right subtree for inorder list
	- then same number of left subtree will be selected sequentially from 1st index of preorder list and rest to right subtree
- recursively call the function
#### mistakes

#### code snippet
```python

```