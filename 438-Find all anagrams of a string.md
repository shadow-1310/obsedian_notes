topic:

### basic info
- source: 
- serial no: #leetcode/438 
- first_done: [[2023-10-27]]
- last_revised: [[2024-06-11]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/find-all-anagrams-in-a-string/
- solution_link: [my solution](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/string/438-find_all_anagram.py#L30-L63)
	- [neetcode solution](https://www.youtube.com/watch?v=G8xtZy0fDKg)
### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- use sliding window approach
#### mistakes
- remember the edge case where len(p) > len(s)
	- simply return [], empty list
- first initialize l=0 and r = n1, because we want to remove l position and add r position
#### code snippet
```python

```