topic:

### basic info
- source: 
- serial no: #leetcode/130 
- first_done: [[2023-10-01]]
- last_revised: [[2023-10-17]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/surrounded-regions/description/
- solution_link: https://www.youtube.com/watch?v=9z2BunfoZ5Y

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- do the reverse thinking, from the border regions whenever encounter a 'O', do dfs and make all its neighbor as unsurrounded category (add to the set)
- BFS approach is lengthy but more memory efficient
#### mistakes
- add node to visited set only after popping it and checking if it non visited
#### code snippet
```python

```