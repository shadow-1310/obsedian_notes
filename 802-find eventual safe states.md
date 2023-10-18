topic:

### basic info
- source: 
- serial no: #leetcode/802 
- first_done: [[2023-10-01]]
- last_revised: [[2023-10-18]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/find-eventual-safe-states/description/
- solution_link: [Neetcode solution]
	- [my solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/graph/802-find_safe_states.py)

### approach - 1
- Time Complexity $$TC = O(E+V)$$
- space complexity

#### pseudo code
- it can be done using two approaches with DFS, neetcode shows one way of using a single hashmap to check whether the current node is safe or not and also if it is visited
- in my solution I have used 2 different sets to determine it, it increases the space complexity
#### mistakes
- append current visited node to safe before returnung True
#### code snippet
```python

```