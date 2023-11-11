topic:

### basic info
- source: #coding-ninjas
- serial no: 
- first_done: [[2023-11-11]]
- last_revised:
- difficulty:
	- [x] easy
	- [ ] medium
	- [ ] hard
- problem_link: https://bit.ly/3MC5iAx
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code

#### mistakes

#### code snippet
```python
def findMissingRepeatingNumbers(a: [int]) -> [int]:
    # Write your code here
    seen = set()
    tot = 0
    n = len(a)
    for num in a:
        tot += num
        if num in seen:
            duplicate = num
        seen.add(num)

    curr = tot-duplicate
    actual = n*(n+1) >> 1
    return [duplicate, actual-curr]
```