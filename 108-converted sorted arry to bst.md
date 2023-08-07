topic:

### basic info
- source: #leetcode 
- serial no: #leetcode/108
- first_done: [[2023-06-27]]
- last_revised:
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/description/
- solution_link: https://www.youtube.com/watch?v=0K0uCMYq5ng

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- make a helper function which will take left and right index to make a node.
- helper function will use left and right to calculate mid index and create a new node with this mid index value
	- then it connect the left child giving the left half of the data
	- and connects the right child with the right half
#### mistakes
- call left on (left, mid-1) not (0, mid-1), similarly for right child (mid+1, right)
- create new node with value in mid index <code>node = TreeNode(nums[mid])</code>
#### code snippet
```python

```