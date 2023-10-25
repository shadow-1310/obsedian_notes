topic: 

### basic info
- source: 
- serial no: #leetcode/322
- first_done: [[2023-09-20]]
	- 1st_revised:[[2023-10-09]]
- last_revised:[[2023-10-25]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/coin-change/
- solution_link: [bottom-up approach](https://www.youtube.com/watch?v=H9bfqozjoqs)
	- [top down approach](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/1DP/322-coin_change.py#L15-L38)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- there are 2 approaches to this problem
	- one is top-down
	- other is bottom up
- although bottom-up is more efficient and compact, it is less intuitive for me
#### mistakes
- use float('inf') for paths where it is not possible to reach amount
- in bottom up approach, only update cache if rem-coin >= 0 else index out of error will occur
#### code snippet
```python

```