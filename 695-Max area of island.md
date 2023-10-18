topic:

### basic info
- source: 
- serial no: #leetcode/695 
- first_done: [[2023-10-01]]
- last_revised:[[2023-10-18]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/max-area-of-island/description/
- solution_link: [my solution on github using BFS](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/graph/695-max_area_island.py)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- similar to [[200-Number of islands]] , instead of  counting islands introduce a area parameter for each call of dfs
- store all area in a list and return the max of this list
#### mistakes
- include the edge case when input grid doesnot have any island, max_area will be empty so return 0
- before incrementing current area check if current node is already visited.f
#### code snippet
```python

```