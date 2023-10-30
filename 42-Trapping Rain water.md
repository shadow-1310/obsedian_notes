topic:

### basic info
- source: 
- serial no: #leetcode/42 
- first_done: [[2023-10-30]]
- last_revised:
- difficulty:
	- [ ] easy
	- [ ] medium
	- [x] hard
- problem_link: https://leetcode.com/problems/trapping-rain-water/description/
- solution_link: https://www.youtube.com/watch?v=ZI2z5pq0TqA

### approach - 1
- Time Complexity: $$O(N)$$
- space complexity$$O(N)$$

#### pseudo code
- keep track of left max
- keep track of right max
- if curr < min(left_max, right_max)
	- res += min(left_max, right_max) - curr
#### mistakes
- memory complexity can be reduced to O(1), have to NC tutorial
#### code snippet
```python

```