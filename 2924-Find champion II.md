topic:

### basic info
- source: 
- serial no: #leetcode/2924 
- first_done: [[2023-11-05]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/find-champion-ii/description/
- solution_link: [my solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/contest/2924-find_championII.py)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- make the adjacency list **A** but in reverse, where A[i] represents list of nodes pointing to i
- Now  run a loop on A 
	- if len(A[i]) == 0, then i is a potential champion, so append it to res
- but if we find more than one champion we return -1 else return res[-1]
#### mistakes

#### code snippet
```python

```