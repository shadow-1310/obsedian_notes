topic: #dsa/heap [[Heap]]

### basic info
- source: 
- serial no: #leetcode/378
- first_done: [[2023-07-09]]
	- 1st_revised: [[2023-08-29]]
- last_revised: [[2023-10-16]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/description/
- solution_link: https://leetcode.com/problems/kth-smallest-element-in-a-sorted-matrix/solutions/1322101/c-java-python-maxheap-minheap-binary-search-picture-explain-clean-concise/

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- first add all 1st col elements to the minheap
- then whenever possible insert the next col element
#### mistakes
- don't take the matrix elements in a list and then heapify, instead directly iterate through the elements and heappush it.
#### code snippet
```python

```