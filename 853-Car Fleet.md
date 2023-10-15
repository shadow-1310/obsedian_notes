topic:

### basic info
- source:  
- serial no: #leetcode/853 
- first_done: [[daily-notes/2023-06-06|2023-06-06]]
- last_revised: [[2023-09-21]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/car-fleet/description/
- solution_link: https://www.youtube.com/watch?v=Pr6T-3yB9RM

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- Sort the given position list in descending order and zip it with speed
- traverse the list and calculate time required by it to reach target to the stack.
- for the next car ( behind the first car or less in position) also calculate time required. if `time(second) ≤ time(first)` then `pop()`
#### mistakes

#### code snippet
```python

```