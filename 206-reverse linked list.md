topic:

### basic info
- source: #leetcode 
- serial no: #leetcode/206
- first_done:
- last_revised: [[2023-08-30]]
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/reverse-linked-list/description/
- solution_link: https://www.youtube.com/watch?v=G0_I-ZF0S38

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- maintain two pointers `curr` and `prev`
- iterate through the linked list and change `curr.next](<http://curr.next>) = prev` but before that save curr.next in other variable and use this variable to chage curr
#### mistakes
- don’t return the head as after the last loop it will become None
    - return the prev or tail
#### code snippet
```python

```