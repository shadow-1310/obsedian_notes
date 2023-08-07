topic: #dsa/heap [[Heap]]

### basic info
- source: #leetcode 
- serial no: #leetcode/973
- first_done: [[2023-07-07]]
	- 1st revised:[[2023-07-17]]
- last_revised: [[2023-08-06]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/k-closest-points-to-origin/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- iterate through the given points list and replace each point with a tuple having (dist, [x,y])
- now heapify this whole list
- again iterate through the heap(min heap) and pop the top element and append to the *res*.
- break the loop when len(res) == k
#### mistakes

#### code snippet
```python

```