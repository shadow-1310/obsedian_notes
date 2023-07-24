topic:

### basic info
- source: #leetcode  
- serial no: #leetcode/647 
- first_done: [[2023-07-24]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [here](https://leetcode.com/problems/palindromic-substrings/description/)
- solution_link: [Palindromic Substrings - Leetcode 647 - Python - YouTube](https://www.youtube.com/watch?v=4RACzI5-du8)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- iterate through the string char by char
- consider each char as middle character of the substring and assign a left and right pointer 
- update the left and right pointer as 
<code>left = left-1</code>
<code>right = right +1</code>
- run the loop till left >= 0 and right < len(s) and s[left] == s[right]
- and increase count by 1 each time
#### mistakes

#### code snippet
```python

```