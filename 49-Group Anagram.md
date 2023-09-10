topic: #dsa/array #dsa/bucketlist

### basic info
- source: #leetcode 
- serial no: #leetcode/49 
- first_done:
- last_revised: [[2023-09-10]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/group-anagrams/description/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- initialize a empty hashmap
- for every word in the `strs` create a unique list which contains count of 26 alphabets from a-z
- this list will serve as a key in our hasmap for which value will be the word itself.
- if in our future iteration we find a similar key, we will add it to the existing list of words.

Note:

- we cannot use the actual list as key of our hashmap as python does not permit mutable datatype to be keys of a dict
- so we have to convert list into tuple which is immutable, we don't use set as set doesn't allow duplicate entries
#### mistakes

#### code snippet
```python

```