topic: #dsa/backtracking 

### basic info
- source:  #leetcode 
- serial no: #leetcode/46
- first_done: [[2023-07-11]]
	- 1st revise: [[2023-07-27]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/permutations/description/
- solution_link: [Link](https://www.youtube.com/watch?v=Nabbpl7y4Lo) 
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/Nabbpl7y4Lo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- base case is if len(curr) == len(nums), then append curr to res and return 
- if base case len(curr) > n, return
- function will take two input parameter, 
	- curr and used (hashmap or boolean array)
	- use a loop in the range 0 to len(nums)
		- execute inner block only if i-th value is not used, we can know it using our hashmap or boolean array
		- append i-th value to curr, update hashmap/array
		- recursive call with updated curr and *used*
		- pop last added element from curr and update *used*
		- continue the loop
#### mistakes / improvments
- boolean array is good alternative to hashmap
#### code snippet
```python

```