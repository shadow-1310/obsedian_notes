topic:

### basic info
- source: #leetcode 
- serial no: #leetcode/128 
- first_done:
- last_revised: [[2023-09-08]]
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
#### code snippet
```python

```