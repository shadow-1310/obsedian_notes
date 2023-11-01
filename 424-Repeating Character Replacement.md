topic:

### basic info
- source: 
- serial no: #leetcode/424
- first_done: [[2023-05-30]]
	- 1st_revised: [[2023-09-06]]
- last_revised: [[2023-11-01]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/longest-repeating-character-replacement/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- use sliding window approach, maintain left and right pointer
- use a helper function which can calculate max freq given a hashmap
- whenever we see right element we append it to current hashmap
	- increment if already exists
	- set to 1 if new
- then check tot-max_freq <= k, then check if curr_len is max
- else increment left by 1
- eitherway increment right pointer
#### mistakes
- don't forget to put the equal sign in loop condition left <= right
#### code snippet
```python

```