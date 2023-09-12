topic:

### basic info
- source: #gfg 
- serial no: 
- first_done: [[2023-01-27]]
	- first revised: [[2023-02-12]]
- last_revised:[[2023-09-12]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://practice.geeksforgeeks.org/problems/count-pairs-with-given-sum5022/1
- solution_link: [my solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/GFG/array/count_pairs_given_sum.py#L27-L43)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- similar to [[1-Two Sum]], but here we also update the key-value in hashmap if it already exists and we increament count by the value in the hashmap.
- check if the element exists in the hashmap if not store the difference to target in the hashmap as a key
	- and for the value if it already exists then increament.
#### mistakes
- don't use 2 loops
- we have to check if (k -num) exists in the hashmap to update key-value, do not check for num
#### code snippet
```python

```