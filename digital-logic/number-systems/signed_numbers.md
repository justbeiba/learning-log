## How do we find 1's complement and 2's complement?
Binary = 11000101
1's complement = 00111010 (invert bits)

2's complement = 00111011 (add 1)
## Why do we need 1's complement and 2's complement?
Computers use them to perform addition and subtraction. 2’s complement allows subtraction to be performed using addition only, which simplifies hardware design.
## Understanding 1's complement.
Let's use 4-bit binary representation.

2^4 = 16 possible numbers can be represented.

From 0000 to 1111, where MSB (first digit) shows the sign. If 0 it is a positive, if 1 it is a negative number.

```
0000 = +0
0001 = +1
0010 = +2
...
0111 = +7
1000 = -7
...
1101 = -2
1110 = -1
1111 = -0
```
1's complement has two representations of zero (+0 and -0), which complicates arithmetic operations.

If you noticed, this can be presented as a circle:

<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/93b02640-02c5-44c8-806c-882919d6ee59" />

Source: Wikipedia (https://en.wikipedia.org/wiki/Ones%27_complement).
## Understanding 2's complement.
Same 4-bit binary representation.

However, in 2's complement, negative numbers are represented by taking the 2's complement of their positive value.

So, 1111 is no longer -0 but -1. 0001 is +1, 1110 is -1 in 1's complement, add +1 to it and we get 1111 representing the same -1.
```
0000 = 0
0001 = +1
0010 = +2
...
0111 = +7
1000 = -8
1001 = -7
...
1110 = -2
1111 = -1
```
Modern computers use 2’s complement.
