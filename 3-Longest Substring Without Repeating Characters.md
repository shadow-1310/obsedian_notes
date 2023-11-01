topic:

### basic info
- source: 
- serial no: #leetcode/3
- first_done: [[2023-05-30]]
	- 1st_revised: [[2023-06-02]]
	- 2nd_revised: [[2023-09-06]]
	- 3rd_revised: [[2023-10-27]]
- last_revised: [[2023-11-01]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/longest-substring-without-repeating-characters/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- initialize a dictionary `seen_map` and two pointer `left` and `right`
- iterate through the string and store the index of each character to the dictionary
- if the current char is found in the dictionary and it is towards the right of the left pointer, then move the left pointer to `seen_map[char] + 1`
- after each iteration count length of current sequence by `right - left + 1` and compare it with `max_count`, if found more update `max_count`
#### mistakes
- put the breaking condition of encountering previously seen character as index >= left instead left > index
- don't forget to add the current char to seen map
#### code snippet
```python

```