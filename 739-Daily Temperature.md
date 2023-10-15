topic:

### basic info
- source: 
- serial no: #leetcode/739 
- first_done: [[daily-notes/2023-06-06|2023-06-06]]
- last_revised: [[2023-09-21]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/daily-temperatures/description/
- solution_link: https://www.youtube.com/watch?v=cTBiBSnjO3c

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- maintain a monotonic stack which stores `[temp, index]` which doesn’t seen day with more temperature
- if a day with more temperature encountered then update `res` and pop() from stack till condition is met
#### mistakes
- only pop() when value is strictly increasing > not ≥
#### code snippet
```python

```