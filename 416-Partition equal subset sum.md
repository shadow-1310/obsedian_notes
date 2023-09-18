topic: [[Dynamic Programming]]

### basic info
- source: #leetcode 
- serial no: #leetcode/416
- first_done: [[2023-07-25]]
- last_revised: [[2023-09-18]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/partition-equal-subset-sum/description/
- solution_link: [Partition Equal Subset Sum - Dynamic Programming - Leetcode 416 - Python - YouTube](https://www.youtube.com/watch?v=IsvocB5BJhw)

### approach - 1
- Time Complexity $$TC = O(N*sum(nums))$$
- space complexity $$SC = O(sum(nums))$$

#### pseudo code
- initialize a set which will store all the possible combination sum till now
- iterate through the given nums from backwards
#### mistakes
- don't try to append the curr_sum to the set, because we are iterating through that set
- instead create a temp set and store all the values in it, after the loop of the original set ends, assign this temp set to original set
#### code snippet
```python

```