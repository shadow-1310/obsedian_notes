topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: 
- serial no: #leetcode/77
- 1st done: [[2023-07-26]]
- last_revised: [[2023-10-06]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: 
- solution_link: [Link](https://www.youtube.com/watch?v=q0s6m7AiM7o)
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/q0s6m7AiM7o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
### approach - 1
- Time Complexity: $$O(N) = k*N^k$$
- space complexity

#### pseudo code
- we need to make a helper function to backtrack
	- it will take 2 parameters, start and curr
	- it will append start element to curr then call the function with backtrack(start+1, curr)
	- then it will pop from curr and append (start+1) and call (start +1 +1)
	- this loop will go till start becomes N
- base case is len of curr becomes then we append curr to res and return 
- another base case is if start > N *or* len(curr) > k
#### code snippet
```python
from typing import List

class Solution:
	def combine(self, n: int, k: int) -> List[List[int]]:
		res = []
		
		def dfs(start, curr):
			if len(curr) == k:
				res.append(curr.copy())
				return
			
			if len(curr) > k or start > n:
				return
			
			for j in range(start, n+1):
				curr.append(j)
				dfs(j+1, curr)	
				curr.pop()
				
	dfs(1, [])
	return res

s = Solution()
print(s.combine(4, 2))
```

##  mistakes
- don't call the original function in a loop, we need to call it only once with backtrack(1, [])
- you can't call the dfs function like <code>dfs(j+1, subset.append(j))</code> because <code>subset.append(j)</code> argument will modify subset in place and will pass None as an argument to the function call.  ^d6d060
	- Instead do the following inside the loop
		-  append first 
		- then call dfs 
		- then pop
- no need to maintain the record of visited nodes