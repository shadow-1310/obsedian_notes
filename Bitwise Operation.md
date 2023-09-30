## Basic Overview
- https://www.youtube.com/watch?v=Db8OmMfzwl8
- https://www.youtube.com/watch?v=h7meukyY_bQ
- https://www.youtube.com/watch?v=bTauscvOymA

#### substraction
- use 2's complement 
#### divide by 2 
- right shift by 1
#### multiply by 2 
- left shift by 1
#### check odd/even number
- mask with 1 (number & 1), if result is 1 then number is odd
- mask with 1 (number & 1), if result is 0 then number is even

#### swap two numbers using XOR
- a=a^b
- b=a^b
- a=a^b

### Bit masking
#### get ith but
- create  1 mask by shifting 1, i-th times to the left
	- 1 << i
- do & operation with the number
	- if result is 1 then ith bit is 1
	- if result is 0 then ith bit is 0
#### set ith bit
- create a mask by left shifting 1 by ith times, 1 << i
- perform or operation of this mask with original number, n = n | mask
#### clear ith bit
- create a mask by left shifting 1 by ith times, 1 << i, then take invert of this number
	- ~(1 << i)
- perform & operation of this mask with original number, n = n & mask

#### Find number of bits to required for changing a to b
- do XOR operation, here we will get 1s where bits were different
- now count number of bits in the number by following method.
#### find numbers of set bit
- do <code>n & (n-1)</code>
	- which makes least significant set bits to 0.
- the number of times required to make it equal to 0 = number of set bits
### Implementation from scratch
#### pseudo-code

#### code

## Related Problems
---
- [[191-Number of set bits]]
- [[136-Single Number]]


