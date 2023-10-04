topic: [[Tree]]

### basic info
- source: 
- serial no: #leetcode/110
- first_done: [[2023-06-17]]
	- first_revised: [[2023-07-31]]
- last_revised: [[2023-10-04]]
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/balanced-binary-tree/description/
- solution_link: https://www.youtube.com/watch?v=QfJsau0ItOY

### approach - 1
- Time Complexity
- space complexity 

#### pseudo code
- use a helper function which takes one argument as input, node
- and return list of 2 elements as output
	- first element is whether current node is balanced or not, True or False
	- 2nd element is height of current node
		- height(current) is calculated by 1 + max(height(left), height(right))
- base case is if current node is None return  [True, 0]
- current node will return balanced = True only if left and right subtree is balanced and abs(height(left) - height(right)) <= 1

#### mistakes
- finally don't return dfs(root)
	- you need to return dfs(root)[0]
#### code snippet
```python

```