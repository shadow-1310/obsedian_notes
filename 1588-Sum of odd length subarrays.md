topic:

### basic info
- source: 
- serial no: #leetcode/1588 
- first_done: [[2023-11-10]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/sum-of-all-odd-length-subarrays/description/
- solution_link: https://www.youtube.com/watch?v=J5IIH35EBVE
	- [my solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/array/medium/1588-sum_odd_length_subarray.py#L33-L47)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- if a number appears in N subarrays, then it will appear in N/2 odd  length subarrays if N is even and (N/2+1) odd length subarrays if N is odd
- we can find for an index i by, 
	- N = (subarrays starting from i) x (subarrays ending at i)
	- N = (n-i) x (i+1), where n=total number of elements
#### mistakes

#### code snippet
```python

```