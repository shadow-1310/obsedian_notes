topic:

### basic info
- source:  #leetcode 
- serial no: #leetcode/347
- first_done:
- last_revised: [[2023-09-07]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/top-k-frequent-elements/
- solution_link:

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- to store the numbers in a list at a index position which is their frequency. this is called bucket list. So bucket list is a list of list like these `[ [], [], [], [], [] ]`
- first iterate through the given list and make frequency hashmap based on that. tihs hashmap will have number as keys and their frequency as values
- next initialize an empty bucket list with max_index equal to length of given list.
- iterate through the frequency hash map and take values as the index of the bucket list and append the corresponding key to that index position of bucket list.
- finally iterate through the bucket list from the last position and add the list elements to result list. if `len(result) == k`. return the result list
#### mistakes
- make the bucket list as len(nums)+1 not len(nums)
#### code snippet
```python

```