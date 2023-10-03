topic: #dsa/linked-list [[Linked List]]

### basic info
- source: 
- serial no: #leetcode/143
- first_done: [[2023-06-09]]
	- first_revised: [[2023-09-02]]
- last_revised: [[2023-10-03]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/reorder-list/description/
- solution_link: https://www.youtube.com/watch?v=S5bfdUTrKLM

### approach - 1
- Time Complexity
- space complexity

#### pseudo code

#### mistakes
- don't initialize slow and fast pointer in same position, otherwise it will lead to cycle in case of even list
	- slow=head
	- fast = head.next
- in the last loop while reordering keep the base condition for both pointer to be non null
#### code snippet
```python

```