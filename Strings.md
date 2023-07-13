tags : #datatypes #unfinished 
- they are immutable datatypes

##### to add a element

^9dd74b

- we can't add a element to end in O(1) just like append in list
- Following are some methods - 
	- String concatenation,  string + 'c'
		- it concatenates two string variable 
		- even if we only want to append to the end one character, it will copy first string and then concatenate to the second
##### to remove last element

^2df1dd

- as they are immutable we cannot remove the last element in O(1) time just like pop() method of list ^489546
- Following are some methods to use
	- String slicing
		- use string[:-1], but it takes O(N) time complexity