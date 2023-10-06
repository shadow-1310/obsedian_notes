topic: #dsa/backtracking 

### basic info
- source: 
- serial no: #leetcode/78 
- first_done: [[2023-07-12]]
	- 2nd done: [[2023-07-28]]
- last_revised: [[2023-07-10]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/subsets/description/
- solution_link: https://www.youtube.com/watch?v=REOH22Xwdkk

### approach - 1
- Time Complexity: $$ O(n*2^n)$$
- space complexity

#### pseudo code
- need to do dfs 
- base case is if *i >= len(nums)*, append the subset to res and return None
- at each node we will split 2 branch, 
	- one with appending current index
	- another with not append current index
- So at each level we will make decision for the current index at that level like below diagram, here we see first level is only for 1st index, 2nd level is making decision only for 2nd index similarly 3rd level is for 3rd index
	![[Pasted image 20230711235340.png]]
#### mistakes
-  append the copy of the subset not the original subset as it will change later
#### code snippet
```python
from typing import List

class Solution:

	def subsets(self, nums: List[int]) -> List[List[int]]:
	
		subset = []
		res = []
		
		def dfs(i):
			if i >= len(nums):
				res.append(subset.copy())
				return
			
			subset.append(nums[i])
			dfs(i+1)
					
			subset.pop()
			dfs(i+1)
		
	dfs(0)
		
	return res
```