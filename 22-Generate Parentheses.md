topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: #leetcode
- serial no: #leetcode/22
- first_done: [[2023-07-13]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [link](https://leetcode.com/problems/generate-parentheses/description/?envType=featured-list&envId=top-interview-questions)
- solution_link: [Generate Parentheses - Stack - Leetcode 22 - YouTube](https://www.youtube.com/watch?v=s9fokUqJ76A&t=707s)
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/s9fokUqJ76A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- we will have a backtrack helper function, it will take 3 input parameters
	- open, current number of '(' parentheses
	- close, current number of '')' parentheses
	- curr, current subset
- base case is <code>open == close == n</code>
	- join the current subset to make it a string using <code>''.join(curr)</code> 
- at each node we will have 2 decision,
	- to insert a '(' parentheses
	- or to insert a ')' parentheses
- but we will insert ( only if <code>open << n</code>
	- update open count
	- before calling the next recursive function pop() from curr.
- and insert ) only if <code>close << open</code>
	- update open count
	- before calling the next recursive function pop() from curr.
#### mistakes

#### code snippet
```python

```