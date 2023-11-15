topic:

### basic info
- source: 
- serial no: #leetcode/238 
- first_done: [[2023-06-01]]
	- 1st_revised: [[2023-09-07]]
	- 2nd_revised: [[2023-10-14]]
- last_revised: [[2023-11-15]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/product-of-array-except-self/
- solution_link: [Neetcode](https://www.youtube.com/watch?v=bNvIQI2wAjk)
	- [easy explaination](https://www.youtube.com/watch?v=5bS636lE_R0)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- initialize product array with 1
- first iterate through the product array and multiply each element with preproduct
- then iterate from the backside and multiply with the post product
	- use a temp variable for storing and updating the post product
#### mistakes
- for the post product use a temp variable and multiply with current index value in product array
	- don't multiply with product[i-1]
#### code snippet
```python

```