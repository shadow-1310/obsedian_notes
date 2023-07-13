topic: #dsa/backtracking 

### basic info
- source: #leetcode 
- serial no: #leetcode/39
- first_done: [[2023-07-11]]
- last_revised:
- difficulty: 
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/combination-sum/description/
- solution_link:
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/GBKI9VSKdGg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### approach - 1
- Time Complexity: $$ O(N) = 2^t, where, t=target$$
- space complexity

#### pseudo code
- can be done with a decision tree, where at each decision tree we take 2 decision
	- first decision is selection the same index to append
	- second decision is not to take the same index
- base conditions are sum == target and i >=len(candidates) or sum > target
- then append current i-th value and again call the function on i-th value
- pop the appended value and call the function on next index

#### mistakes
- in current sub list append only a copy as the original will get modified
#### code snippet
```python
from typing import List
#correct solution done with recursive approach where no duplicates are allowed
#done on 11-07-2023

class Solution:

	def combinationSum(self, candidates: List[int], target: int) -> List[List[int]]:	
	res = []

	def dfs(i, curr, sum):
		if sum == target:
			res.append(curr.copy())
			return
			
		if i >= len(candidates) or sum > target:
			return
		
		curr.append(candidates[i])
		dfs(i, curr, sum + candidates[i])
		
		curr.pop()
		dfs(i+1, curr, sum)	  
	
	dfs(0, [], 0)
	return res
```