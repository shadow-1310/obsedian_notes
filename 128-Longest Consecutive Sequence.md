topic:

### basic info
- source: 
- serial no: #leetcode/128 
- first_done: [[2023-06-01]]
	- 1st_revised: [[2023-09-08]]
- last_revised: [[2023-10-14]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/longest-consecutive-sequence/
- solution_link: https://www.youtube.com/watch?v=P6RZZMu_maU

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- main idea is to convert the given list into **set** which can be used as an hashmap
- then iterate through the set and start counting the range only if its previous element (num-1) does not exist in the set.
#### mistakes
- continue the if condition only if the previous number doesnot exist in the set.
- define the res variable outside the loop
#### code snippet
```python

```