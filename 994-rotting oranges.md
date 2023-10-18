topic:

### basic info
- source: 
- serial no: #leetcode/994 
- first_done: [[2023-10-02]]
- last_revised: [[2023-10-18]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/rotting-oranges/description/
- solution_link: https://www.youtube.com/watch?v=y704fEOx0s0

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- perform multisource BFS
#### mistakes
- run the parent loop tile fresh != 0
- when using a visited set, careful when to decreament fresh
	- whenever visiting a node , don't always decrease fresh, first check if visited element is 1 or not, because initially we also appended 2 to the queue
- while using visiting set it becomes complex, don't use visited set, instead 
#### code snippet
```python

```