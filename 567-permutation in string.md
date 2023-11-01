topic:

### basic info
- source: 
- serial no: #leetcode/567
- first_done: [[2023-05-31]]
	- 1st_revised: [[2023-09-07]]
- last_revised: [[2023-09-07]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/permutation-in-string/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- map string1 and string2 with a list where character index will be ord(char) - ord('a')
- then make a sliding with left and right. where,left = 0 and  right = left + len(s1) - 1
- at each iteration check if the maps matches with a helper function and update the map
#### mistakes
- initialize right pointer to be left + len(s1) -1, remember the **-1**
- don't forget base condition of len(s1) > len(s2), where we'll directly return False
	- forgot this again on [[2023-11-01]]
- map string 1 and string 2 first characters in the same loop
#### code snippet
```python

```