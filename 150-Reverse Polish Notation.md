topic: [[Stack]]

### basic info
- source: 
- serial no: #leetcode/150 
- first_done: [[daily-notes/2023-06-06|2023-06-06]]
- last_revised: [[2023-07-21]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/evaluate-reverse-polish-notation/description/
- solution_link: https://www.youtube.com/watch?v=iu0082c4HDE

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- use an stack 
- then iterate through the tokens
	- if we encounter a non operator/digit, append it to to the stack
	- if we encounter a operator, pop the last 2 digit of the stack and perform the operation to get a new value. Then append the new value to the stack
- return only remaining element in stack
#### mistakes
- don't use floor division operator for <code>'/'</code>, as for -ve numbers it gives wrong results.
- use an predefined set having (+, -, *, ''/'') to identify if the encountered element is operator or digit. it will be faster than using a list
#### code snippet
```python

```