topic: #dsa/backtracking [[Backtracking]]

### basic info
- source: 
- serial no: #leetcode/79 
- first_done: [[2023-07-13]]
- last_revised: [[2023-10-06]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/word-search/description/ 
- solution_link: [Word Search - Backtracking - Leetcode 79 - Python - YouTube](https://www.youtube.com/watch?v=pfiQ_PS1g8E)
	- <iframe width="560" height="315" src="https://www.youtube.com/embed/pfiQ_PS1g8E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### approach - 1
![[Pasted image 20230713185542.png]]
- Time Complexity $$TC = O(r*c*4^N)$$
- space complexity

#### pseudo code
- backtrack function will have 3 input parameters, r,c,i
	- r is row number
	- c is column number
	- i is current index of the word we are searching
- base case is <code>i == len(word)</code>
	- return True
- one more base case is r,c < 0 or <code>r,c >= len(word)</code> or (r,c) in already traveled path or <code>board[r][c] !=word[index]</code> 
	- return False
- other wise append current cell index (r,c) to path then call backtrack function on surrounding 4 cells, up, down, left and right 
- after call remove appended cell value (r, c)
#### mistakes
- never forget to include all the base cases
	- r, c >= len(word)
	- r, c < 0
	- <code>board[r][c] !=word[index]</code> 
	- (r,c) in path
- set the rows and cols properly
#### code snippet
```python

```