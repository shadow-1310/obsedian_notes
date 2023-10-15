topic:
- have to find the MEX (Minimum Excluded) of an array after performing some operations
### basic info
- source: 
- serial no:
- first_done:
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: [discussion](https://leetcode.com/discuss/interview-question/1799446/mercari-inc-software-engineer-new-graduate-position-hiring-test-2022)
- solution_link: [my git solution](https://github.com/shadow-1310/DSA_practice/blob/master/company_specific/mercari_japan/find_max_MEX.py)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- reduce each element to be between 0 to X-1
	- we can do this by performing (element % X)
- then get count of elements in this array
- MEX = **least count number + count of least count number * X**
#### mistakes

#### code snippet
```python

```