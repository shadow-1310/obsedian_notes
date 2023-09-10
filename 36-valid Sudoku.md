topic:

### basic info
- source: 
- serial no:
- first_done: [[2023-05-24]]
	- first_revised: [[2023-06-11]]
- last_revised: [[2023-09-10]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/valid-sudoku/description/
- solution_link: [my latest solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/array/medium/36.valid_sudoku.py#L95-L131)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- iterate through all the positions with 2 for loops
- if ele == "." then continue
- check if element is in the same row
- check if element is in the same column
- check if element in the same box.
	- find the box range from the element index(i, j)
#### mistakes
- remember that the values are stored as strings so keep in mind when comparing with integers.
- while checking the current row or column or the box, consider also if it the same position or not
	```python
	if board[row][j] == ele and row != i:
		return False
	```

	```python
	if board[i][col] == ele and col != j:
		return False
	```

	 ```python
	if board[row][col] == ele and i != row and j != col:
		return False
	```
#### code snippet
```python

```