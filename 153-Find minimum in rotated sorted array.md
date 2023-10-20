topic:

### basic info
- source: 
- serial no: #leetcode/153 
- first_done: [[2023-05-27]]
	- last_revised: [[2023-09-22]]
- last_revised: [[2023-10-20]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity
### observations (possibility of new problem )
- if we keep count how many loop is required to find minimum, then count+1 gives the rotation of the array
- for ascending order array, it must be rotated len(nums) times
- for descending order array, it must be rotated len(nums)-1 times
#### pseudo code

#### mistakes
- don't forget to include the equal condition, when mid becomes equal to 0th index.
	- repeated same mistake
- keep the base condition when array is already sorted or len(nums) == 1
#### code snippet
```python

```