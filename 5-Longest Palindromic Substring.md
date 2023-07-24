topic:

### basic info
- source: #leetcode  
- serial no: #leetcode/5
- first_done: [[2023-07-24]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [here](https://leetcode.com/problems/longest-palindromic-substring/description/)
- solution_link: [Longest Palindromic Substring - Python - Leetcode 5 - YouTube](https://www.youtube.com/watch?v=XYQecbcd6_c)

### approach - 1
- Time Complexity: $$TC = O(N^2)$$
- space complexity

#### pseudo code
- iterate through the given string char by char
- for each char we will follow two approach, substring with even and substring with odd number of char
- for odd number of characters left and right pointer will start at same position, 
<code>left = right = i</code>
	- then in each loop we will do left = left - 1 and right = right+1
	- and check if s[left] == s[right]
		- count number of character in the substring and if it is more than max_len then update max_len
- for even number of characters 
<code>left = i, right = i+1</code>
#### mistakes

#### code snippet
```python

```