topic: #dsa/tree [[Tree]]

### basic info
- source: #leetcode 
- serial no: #leetcode/102
- first_done: [[2023-06-18]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/binary-tree-level-order-traversal/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- use a deque , deque contains all the nodes in that level, so extract them while also adding their child to the deque.
- while going at each level find the number(N) of nodes in that level and run a for loop N times only to extract nodes , otherwise it will take elements from child
- after the loop ends, it will be filled with child of next level
#### mistakes

#### code snippet
```python

```