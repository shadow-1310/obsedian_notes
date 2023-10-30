topic:

### basic info
- source: 
- serial no: #leetcode/31 
- first_done: [[2023-10-30]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/next-permutation/
- solution_link: [techdose video](https://www.youtube.com/watch?v=6qXO72FkqwM)
	- [striver explaination-better](https://www.youtube.com/watch?v=LuLCLgMElus)

### approach - 1
- Time Complexity: $$TC = O(N)$$
- space complexity: $$SC = O(1)$$

#### pseudo code
- traverse from the right and find an index i such that nums[i] < nums[i+1]
	- if not able to find such index, that means array is in decreasing order, so we simply reverse the array to find the first position, this is the final answer
- after finding such position , we will again traverse from the right and find an index j such that nums[j] > nums[i] and then simply swap these two position 
- now we reverse the array after index i, this is the final answer
#### mistakes

#### code snippet
```python

```