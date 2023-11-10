topic:

### basic info
- source: 
- serial no: #leetcode/560 
- first_done: [[2023-10-24]]
- last_revised: [[2023-11-10]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/subarray-sum-equals-k/description/?envType=study-plan-v2&envId=top-100-liked
- solution_link: [my solution](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/hashing/560-subarray_sumK.py)
	- [neetcode explaination](https://www.youtube.com/watch?v=fFVZt-6sgyo)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- maintain a prefix sum
	- initialize the prefix sum hashmap with {0:1}
- maintain sum upto this element
- at every element we check how much cur_sum is bigger than K, and if we have any prefix that can be subtracted to make it equal to K
- after checking if exists then increment res
- also add curr_sum in the prefix sum dict
#### mistakes

#### code snippet
```python

```