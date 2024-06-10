topic: it is used in spell checker(Levenshtein distance)
![[Pasted image 20231010145149.png]]
### basic info
- source: 
- serial no: #leetcode/72 
- first_done: [[2023-10-10]]
	- 1st_revise: [[2023-10-28]]
- last_revised: [[2024-06-07]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/edit-distance/description/
- solution_link: https://www.youtube.com/watch?v=XYi2-LPrwm4

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
![[Pasted image 20231010140202.png]]
- follow same 2DP approach as [[1143-Longest common subsequence]]
- there are 3 operations as mentioned in the image
	- insert , i,  j+1
	- delete, i+1, j
	- replace, i+1, j+1
#### mistakes
- make the surrounding layer with decreasing values
#### code snippet
```python

```