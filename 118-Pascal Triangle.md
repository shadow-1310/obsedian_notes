topic:

### basic info
- source: 
- serial no: #leetcode/118
- first_done:
- last_revised: [[2023-09-10]]
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/pascals-triangle/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- run two for loop one for total row and one for adding numbers inside row
	- inside the row if it is first element or last element append 1
		- how do we know if it is last element?
		- if j == i
	- else access previous row (except first row), and append the summation of corresponding position element and previous position element.
	- after each loop ends append the current row to final result.
#### mistakes

#### code snippet
```python

```