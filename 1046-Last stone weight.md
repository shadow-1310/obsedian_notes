topic:

### basic info
- source: 
- serial no: #leetcode/1046
	- 1st_done: [[2023-07-06]]
- last_revised: [[2023-10-16]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/last-stone-weight/description/
- solution_link: https://www.youtube.com/watch?v=B-QCq79-Vfw

### approach - 1
- Time Complexity $$TC = O(NlogN)$$
- space complexity

#### pseudo code
- convert all the weight to -ve as python only has min heap
- heapify this list
- iterate through the heap till its empty 
	- proceed only if heap has more than 2 elements else break
	- pop top 2 elements, these are the heaviest one
	- substract one from another
	- if the result is non zero push it to heap else continue
- return 0th element of the heap if it is non empty, if it is empty return 0
#### mistakes
- don't try to do <code>stones = (-1)*stones</code>
	- use list comprehension instead
- don't always return stones[0], check if stones is empty then return 0
#### code snippet
```python

```