topic: #dsa/heap 

### basic info
- source: 
- serial no: #leetcode/1405
- first_done: [[2023-07-10]]
	- 1st_revised: [[2023-08-29]]
- last_revised: [[2023-10-15]]
- difficulty:
	- [ ] easy
	- [x] medium
	- [ ] hard
- problem_link: https://leetcode.com/problems/longest-happy-string/description/
- solution_link: https://www.youtube.com/watch?v=8u-H6O_XQKE

### approach - 1 : using max-heap
- Time Complexity
- space complexity

#### pseudo code
- initialise a list of tuples with two elements **(-count, char)** and *res* = ""
- iterate through the list and heappush each element only if count != 0 , max-heap is ready
- iterate through the heap till it is empty
	- heappop first element and add the char to *res* only if previous two instances is not char
	- else pop the second element (count2, char2) also and add char2 to *res*
		- increment count2+1 and heapop it if it is non zero, we are doing +1 because original counts are -ve. 
	- now heappush *count* if it is non zero.
- return *res*
#### mistakes
- only heappush count/count2 if it is non-zero
- check res[-1] == res[2] == char only if len(res) > 1
- recheck if the heap became empty before popping the second element, if it is empty break the loop.
	- repeated this mistake again
- don't heapify the original inputs as it can have elements with 0 cant, so check element by element and push only if it is non zero
- keep a mind on on which condition we have to increment count1, i.e first popped element

#### code snippet
```python
from typing import List

import heapq

#this is a correct solution done using max-heap approach

# done on 10-07-2023

class Solution:

	def longestDiverseString(self, a: int, b: int, c: int) -> str:
	
		res = ""
		
		max_heap = []
		
		input_char = [(-a, "a"), (-b, "b"), (-c, "c")]
		
		for count, char in input_char:
		
			if count:
			
				heapq.heappush(max_heap, (count, char))
		
		while max_heap:
		
			count, char = heapq.heappop(max_heap)
			
			if len(res) > 1 and res[-1] == res[-2] == char:
			
				if not max_heap:
				
					break
				
				count2, char2 = heapq.heappop(max_heap)
				
				res += char2
				
				count2 += 1
				
				if count2:
				
					heapq.heappush(max_heap, (count2, char2))
				
			  
			else:
			
				res += char
				
				count += 1
			
			if count:
			
				heapq.heappush(max_heap, (count, char))
			
		
		return res
```