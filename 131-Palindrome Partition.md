topic: #dsa/backtracking 
Related: [[Backtracking]]
### basic info
- source:  #leetcode 
- serial no: #leetcode/131
- first_done: [[2023-07-13]]
	- 2nd done: [[2023-07-29]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/palindrome-partitioning/description/
- solution_link: [solution](https://www.youtube.com/watch?v=3jvWodd7ht0)
	<iframe width="560" height="315" src="https://www.youtube.com/embed/3jvWodd7ht0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
### approach - 1
- Time Complexity: $$O(N) = N*2^N$$
- space complexity

#### pseudo code
![[Screenshot from 2023-07-29 13-19-56.png]]
- make a helper function to check if a string is palindrome or not given its start and end pointer/index
- make backtrack helper function, it will take two arguments as input
	- start, starting index
	- curr, current subset
- base case is if start >= len(s)
- start a loop with end value in range (start, len(s))
	- execute the following if s[start:end+1]  is palindrome
		- so for first node string will be of 1 character, for second node it will be of 2 character starting from start position
		- append the string to current subset 
		- and call the backtrack function with start = end+1
		- pop the last added string from current subset
		- continue the loop 
- end loop
#### mistakes
- be careful with the range in loop, it should be (start, len(s))
- for the string to be appended take care *off by 1 error*, it should be s[start:end+1]
#### code snippet
```python

```