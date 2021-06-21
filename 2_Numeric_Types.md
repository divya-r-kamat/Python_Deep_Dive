## Data Types in Python

The int data type
ex : 0, 10, -100, 100000

How large (magnitude) can a Python int become (positive or negative)?

Integers are represented internally using base2 (binary) digits, not decimal


what is the largest (base 10) integer number that can be represented using 8 bits

255

if negative integers, then 1 bit is reserved to represent the sign of a number, leaving only 7 bits [2^7 - 1]
[-128, 127]
[-2^7, 2^7 -1]


In a 32-bit OS:
memory spaces (bytes) are limited by their address number -> 32 bits
when we create a variable its stored in some memory address, and those memory address are represented by integers
in 32 bit architecture the addresses are limited to 32 bits. 
Every address is a byte, so the maximum of address in bytes is 4294967296 bytes of addressable memory
= 4294967296 /1024 kb = 4194304kb
= 4194304 / 1024 MB = 4096 MB
= 4096 / 1024 GB = 4GB


