
### Comparison based
---
#### Bubble Sort
- how it works
- time complexity
	- avg -> 
	- best case
	- worst case -> O(N^2)

#### Quick Sort (Divide and Conquer)
- how it works
	- choose a pivot(1st, last or middle index)
	- choose 2 pointer (left and right)
		- left pointer will search element greater than pivot
		- right pointer will search element less than pivot
		- whenever they find they stop
	- swap pivot
		- if left < right
			- swap pivot with left
		- if right < left
			- swap pivot with right
	- repeat same technique on left and right segments of pivot
- time complexity
	- avg -> O(NlogN)
	- best case -> O(NlogN)
	- worst case -> O(N^2),
		- sorted array in ascending or descending order
- recurrence relation $$T(N) = T(N/2) + N$$

#### Merge Sort (Divide and Conquer)
- how it works
	- divide till only one element remains
	- merge in bottom-up 
- time complexity
	- avg -> O(NlogN)
	- best -> O(NlogN)
	- worst -> O(NlogN)
- recurrence relation

#### Insertion Sort
insertion sort is stable, relative order of same element doesn't change
insertion sort is in place, no extra space
it is online, works on current element immediately without waiting
[gate smasher video](https://www.youtube.com/watch?v=s9fmGjFY1v0)
- how it works
	- works how we arrange playing cards
- time complexity
	- avg -> 
	- best -> O(N)
		- ascending order
		- swap = 0, O(1)
		- comparison = N-1, O(N)
	- worst -> O(N^2)
		- descending order
		- swap = O(N^2)
		- comparison = O(N^2)
- recurrence relation

#### Selection Sort
it is not stable
it is in place, no extra spaces
[tutorial](https://www.youtube.com/watch?v=Lrd1QaKyok4)
- how it works
	- in first pass it sorts the smallest element in place
- time complexity
	- best case -> O(N^2)
		- swaps = 0
		- comaprison = O(N^2)
	- worst case -> O(N^2)
		- comparison - O(N^2)
		- swaps -> O(N)




## Non comparison based
---
### Radix Sort
- non comparison algorithm
- how it works
	- make all equal digits equal in all number
	- start with LSB and sort the numbers according to digit values
- time complexity
	- O(NK), N -> size of array, k -> no. of digits in largest number
		- 
### Counting sort (best algo when range is defined)
range must be given
- how it works
	- best algorithm when range is given- linear time
		- problem is if max number very high space required will be high
	- constraint is , following should be given 
		- input size, N
		- range, K
- time complexity
	- O(N+K)
	- Space complexity
		- O(k)
### Bucket Sort
[tutorial](https://www.youtube.com/watch?v=E9OccfF9mpI)
- constraints
	- floating point
	- range is [0,1]
- Time complexity - O(N)
	- elements should be uniformly distributed, else time complexity may go up to O(N^2)


