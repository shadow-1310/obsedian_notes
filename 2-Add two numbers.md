topic: #dsa/linked-list [[Linked List]]

### basic info
- source: #leetcode 
- serial no: #leetcode/2
- first_done:
- first_revised: [[2023-08-29]]
- last_revised: [[2023-10-03]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/add-two-numbers/description/
- solution_link: https://www.youtube.com/watch?v=wgFPrzTjm7s

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- take values from each linked list if exists or take it as 0
- then store the carry and add the remainder to a new node
- do it till any one of the l1, l2 or carry is non zero
#### mistakes
- remember the edge cases to continue the loop till carry is non zero.
- add the remainder to curr.next 
	- don't store it in curr
#### code snippet
```python

```