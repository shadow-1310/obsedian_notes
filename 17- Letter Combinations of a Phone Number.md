topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: 
- serial no: #leetcode/17
- first_done: [[2023-07-12]]
	- first_revised: [[2023-07-28]]
- last_revised: [[2023-10-06]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [link](https://leetcode.com/problems/letter-combinations-of-a-phone-number/description/)
- solution_link: [solution](https://www.youtube.com/watch?v=0snEunUacZY)
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/0snEunUacZY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### approach - 1
![[Pasted image 20230713014115.png]]
- Time Complexity $$O(N) = N*4^N$$
- space complexity

#### pseudo code
- initialize a hashmap for each digit (2-9) to its corresponding letters like 2 : 'abc', 3: 'def'
- use a helper backtrack function which will take 2 parameters, i and curr
	- i is index in the given digits
	- curr is current subset (use list instead of string to store)
- base case is i >= len(digits)
	- then convert the current subset list string using .join method and append it to *res*
- if not base case then backtrack, backtracking process is simple as before
	- append the current character 
	- call the backtrack function with next index
	- pop the current character
	- continue the loop

#### mistakes
---
- don't try to use a str datatype for storing the current subset, use a list and then convert it
	- because string datatypes are immutable and we will have hard time removing the last element in O(1) like [[Strings#^489546|here]]
- in converting remember to use ''.join(list) method
- remember to include the edge case where input is empty string
	- immediately return res
- repeated same mistake as above
- don't pass the current character to append

#### code snippet
```python

```