topic:

### basic info
- source: 
- serial no:
- first_done: [[2023-10-05]]
- last_revised:
- difficulty:
	- [ ] easy
	- [ ] medium
	- [x] hard
- problem_link: https://practice.geeksforgeeks.org/problems/subtraction-in-linked-list/1
- solution_link: [my solution on github](https://github.com/shadow-1310/DSA_practice/blob/master/company_specific/paytm/subtract_linked_list.py)
	- [GFG discussion](https://www.geeksforgeeks.org/subtract-two-numbers-represented-as-linked-lists/)
	- or check the editorial solution on the problem page
	- [youtube solution in java](https://www.youtube.com/watch?v=wFbsIPlYhOs)

### approach - 1
- Time Complexity
- space complexity

#### pseudo code
- similar to [[2-Add two numbers]]
- first remove the trailing zeros for both the linked lists
```python
	while l1 and l1.data == 0:
        l1 = l1.next

    while l2 and l2.data == 0:
        l2 = l2.next
```
- then we need to determine which number is bigger
	- make two helper function to get length and to reverse a linked list
		- which number has more length will be bigger
		```python
		if n1 > n2:
        big = l1
        small = l2
		elif n1 < n2:
        big = l2
        small = l1
		```
		- if both number has same length, then we will iterate through both of them and whenever we find an bigger digit that linked list will be bigger
		```python
		else:
        t1 = l1
        t2 = l2
        while t1.data == t2.data:
            t1 = t1.next
            t2 = t2.next

            if not t1:
                return Node(0)

        if t1.data > t2.data:
            big = l1
            small = l2

        elif t1.data < t2.data:
            big = l2
            small = l1
		```
		- if both linked list have same digits till the end directly return 0
- Now reverse both the linked list using the helper function
```python
	big = reverse(big)
	small = reverse(small)
```
- for subtraction, initialize a borrow variable initially to False, if it is True then subtract 1 from digit of bigger number, else do nothing.
	```python
		v1 = big.data if big else 0
        v2 = small.data if small else 0
        if borrow:
            v1 -= 1
            borrow = False
        if v2 > v1:
            borrow = True
            v1 += 10
	```
- now again check if big number digit is less than small number digit, if so add +10 to it and make borrow False
	- then do normal subtraction operation
	```python
	v3 = v1 - v2
	curr.next = Node(v3)
	curr = curr.next
	big = big.next
	small = small.next if small else small
	```
- before returning reverse the number and also remove the trailing zeros
```python
res = reverse(dummy.next)
while res and res.data == 0:
	res = res.next
return res
```
#### mistakes

#### code snippet
```python

```