topic: [[Dynamic Programming]]

### basic info
- source: 
- serial no: #leetcode/300
- first_done: [[2023-07-24]]
	- 1st_revised: [[2023-09-16]]
- last_revised: [[2023-10-12]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [here](https://leetcode.com/problems/longest-increasing-subsequence/description/)
- solution_link: [Longest Increasing Subsequence - Dynamic Programming - Leetcode 300 - YouTube](https://www.youtube.com/watch?v=cjWnW0hdF1Y)

### approach - 1
- Time Complexity: $$TC = O(N^2)$$
- space complexity

#### pseudo code
- we are starting from last index, then checking every element after it
#### mistakes
- don't return lis[0], return max(lis)
- don't do lis[i] = 1 + lis[j], because we have many elements for j and we are trying to find out the max out of it, so do
	- lis[i] = max(lis[i], 1+lis[j])
#### code snippet
```python

```