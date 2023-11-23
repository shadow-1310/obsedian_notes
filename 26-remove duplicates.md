topic:

### basic info
- source: 
- serial no: #leetcode/26
- first_done: [[2023-05-12]]
	- 1st_revised: [[2023-09-10]]
- last_revised: [[2023-09-10]]
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- how this code work
    - uses 2 pointers, one (right) will stop whenever we find an unseen number, left pointer will add the new elements
    - return left
#### mistakes
- first of all we cannot use a iterator (for loop) as the iterator itself is changing, so we have to use a while loop
- we also cannot use sorted() method as it will create a new array which is restricted in the question
#### code snippet
```python

```