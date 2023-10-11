topic: [[Dynamic Programming]]

### basic info
- source: 
- serial no: #leetcode/5
- first_done: [[2023-07-24]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [here](https://leetcode.com/problems/longest-palindromic-substring/description/)
- solution_link: [Longest Palindromic Substring - Python - Leetcode 5 - YouTube](https://www.youtube.com/watch?v=XYQecbcd6_c)
	- [my solution in github](https://github.com/shadow-1310/DSA_practice/blob/master/LeetCode/top_interview/1DP/5-longest_palindromic_substring.py#L35-L75)

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
- if you are doing by using count variable, then initialize count as 0 in starting of odd numbers loop and count as 1 for even number loop
- increment count by 2 each time condition is met both for odd and even loop.
- do not use a extra count variable for current length of palindrome, instead use index of right and left pointer
#### code snippet
```python

```