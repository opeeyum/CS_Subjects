## Must do bitwise manipulation question

### Why bit manipulation?
 Bit manipulation, in some cases, can obviate or reduce the need to loop over a data structure and can give many-fold speed ups, as bit manipulations are processed in parallel, but the code can become more difficult to write and maintain.

### 1. **Write a function that takes an unsigned integer and returns the number of '1' bits it has.**
  > Approach:

   We know that every number in computer is represented in binary form (patteren of 1 and 0).
   We are performring a bit wise AND with the number and shifitng the right most bit to null.
   And we can repeat this until given number becomes Zero.
     
### 2. **Given two integers a and b, return the sum of the two integers without using any arithmetic operations.**
  > Approach:

   Let's try this 3 + 2 = 5 , the carry will be with in the brackets i.e "()"
  ```
    3 => 011 
    2 => 010
        _____
        1(1)01
  ```
  Here we will forward the carry at the second bit to get the result.
  So which bitwise operator can do this ? 
  A simple observation says that XOR can do that, but it just falls short in dealing with the carry properly, 
  but correctly adds when there is no need to deal with carry.
  For Eg:
 ```
  1   =>  001 
  2   =>  010 
  1^2 =>  011 (2+1 = 3)
  ```
  So now when we have carry, to deal with, we can see the result as :
  ```
  3   => 011 
  2   => 010 
  3^2 => 001 
  ````
  Here we can see XOR just fell short with the carry generated at the second bit.
  So how can we find the carry ? 
  The carry is generated when both the bits are set, i.e (1,1) will generate carry, 
  but (0,1 or 1,0 or 0,0) won't generate a carry, so which bitwise operator can do that ? 
  **AND** gate ofcourse.

  To find the carry we can do:
  ```
  3    =>  011 
  2    =>  010 
  3&2  =>  010
  ```
  Now we need to add it to the previous value we generated i.e ( 3 ^ 2), 
  but the carry **should be added to the left bit** of the one which genereated it.
  so we left shift it by one so that it gets added at the right spot.

  Hence (3&2)<<1 => 100
  so we can now do
  ```
  3 ^2        =>  001 
  (3&2)<<1    =>  100
  ```
  Now xor them, which will give 101(5) , we can continue this until the carry becomes zero.
### 3. 
  Let if we have X and Y in Such a way that,
X/2 = Y
then Number of set bits in X - Number of set bit in Y <= 1

eg let X = 7and Y = 3
then 7 / 2 = 3;

7 -> 1 1 1 number of set bit are 3
3 -> 0 1 1 number of set bit are 2

there difference is 3 - 2 <= 1

another eg
X = 12 and y = 6
then 12 / 2 = 6;

12 -> 1100 number of set bit are 2
6 -> 0110 number of set bit are 2

there difference is 2 - 2 <= 1

There can be 2 cases
whether X is Odd or Even

if X is ODD

then the (LSB) Least Significant Bit will always be set and dividing by 2 means right shifting the number by 1 bit.
so if last bit is set and right shift it by 1 bit than the last set bit will be lost.
therfore the new number Y has 1 set bit less than in compare to X
But if X is Even

then LSB will be equal to 0, therefore even we do right shift by1 bit then only this 0 bit will be lost and no set bit got lost
so When we have X has Even,

no of set bit in X = no of set bit in Y
and When X is ODD

no of set bit in X = 1 + no of set bit in Y
