topic:

### basic info
- source: #leetcode  
- serial no #leetcode/103
- first_done: [[2023-06-20]]
- last_revised: [[2023-08-01]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- similar to [[102-Binary Tree level order traversal]] just for every loop change the method of appending and pop from the stack
- use a Boolean variable which will change its value after each for loop ends
- nodes will always be from left to right in the stack
	- so if we are popping from right make sure we are appending from left(append right child first)
	- and when we are popping from left we need append from right(append left child first)
#### mistakes

#### code snippet
```python

```