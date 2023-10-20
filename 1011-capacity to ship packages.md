topic:

### basic info
- source: 
- serial no: #leetcode/1011 
- first_done: [[2023-10-07]]
- last_revised: [[2023-10-20]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [LC](https://leetcode.com/problems/capacity-to-ship-packages-within-d-days/description/)
- solution_link: 

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- similar to [[875-Koko eating bananas]]
	- but here the formula for calculating days will change, as in one day we can lift more than one weight
	- also the min and max will change, min need to be max weight
#### mistakes
- don't make min as 1, because our capacity should lift the maximum weight
- here we are not able to lift the weights in fragments.
- making the mistake of returning mid instead of res which stores minimum mid
#### code snippet
```python

```