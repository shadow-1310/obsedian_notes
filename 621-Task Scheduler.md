topic: #dsa/heap [[Heap]]

### basic info
- source: #leetcode 
- serial no: #leetcode/621
- first_done: [[2023-07-09]]
- last_revised: [[2023-08-29]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/task-scheduler/description/
- solution_link: https://www.youtube.com/watch?v=s8p8ukTyA2I

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- initialize a max heap and an deque
    - max heap stores all tasks available to do now as their frequencies
    - deque keep tracks of time availability of task
- initialization
    - store the count of all unique tasks in as a key-value pair in a `dict`
    - take all values of dict and store the negative of it in min heap implementation of heapq `freq`
    - initialize an empty deque `q`
    - time = 0
- start a loop which will continue till heap or deque any of it is non empty and at starting of each loop make `time = time + 1`
    - if heap is non empty remove element from it and add 1. `val = val + 1`
        - if value is now non zero append it to deque as a list of [value, time].
            - where value is `val`
            - and `time = time + n`
    - now check if deque is non empty and time in first element is equal to current time append it to the heap
#### mistakes

#### code snippet
```python

```