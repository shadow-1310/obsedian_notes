topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: #leetcode 
- serial no: #leetcode/40
- first_done: [[2023-07-13]]
	- 2nd done : [[2023-07-28]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/combination-sum-ii/description/
- solution_link: [Combination Sum II - Backtracking - Leetcode 40 - Python - YouTube](https://www.youtube.com/watch?v=rSA3t6BDDwg)
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/rSA3t6BDDwg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### approach - 1
- Time Complexity $$O(N) = N*2^N$$
- space complexity

#### pseudo code
- almost similar as [[39-Combination_Sum]]
- can be done with a decision tree, where at each decision tree we take 2 decision
	- first decision is appending the current index 
	- second decision is not appending the current index
- base conditions are sum == target and i >=len(candidates) or sum > target
- then append current i th index and again call the function on (i+1) th index
- pop the appended value and call the function on (i+1) index
#### mistakes
- don't forget to return res
- don't try to use for loop here. use dual decision at each node concept
#### code snippet
```python

```