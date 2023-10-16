topic: [[Heap]] #dsa/heap 

### basic info
- source: 
- serial no: #leetcode/215
- first_done: [[2023-06-01]]
	- 1st revision : [[2023-07-07]]
	- 2nd revision: [[2023-08-10]]
- last_revised: [[2023-10-16]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/kth-largest-element-in-an-array/
- solution_link: https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/sorting/215.kth_largest_element.py

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- make each number -ve in the given list and store in place using list comprehension
- heapify the list
- initialize a counter with 0
- iterate through the heap and pop element and store it and for each iteration increase counter variable
	- when counter == k; break the loop
- return the last popped element
#### mistakes

#### code snippet
```python

```