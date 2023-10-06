topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: 
- serial no: #leetcode/40
- first_done: [[2023-07-13]]
	- 2nd done : [[2023-07-28]]
- last_revised: [[2023-10-06]]
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
- there are to way to do mistake here
	- consider all the duplicate number in all calls
	- donot use the duplicates in any call
- instead use duplicate in left call and skip them in right call
	- left call is including the current index
	- right call is excluding the current index
#### code snippet
```python

```