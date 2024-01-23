**Bits and Bytes**
- Bit - smallest unit (stores 0 or 1)
- Byte - 8 bits, smallest item we can create a varibale out of

**The Operators**

```cpp
short x = 6891;
short y = 11318;

//& operator, x & y
	 x:  00011010 11101011
	 y:  00101100 00110110
--------------------------
 result: 00001000 00100010    // this is the value 2082

// | operator, x | y
	 x:  00011010 11101011
     y:  00101100 00110110
--------------------------
 result:  00111110 11111111    // this is the value 16127

// ^ operator, x ^ y
	 x:  00011010 11101011
     y:  00101100 00110110
--------------------------
 result:  00110110 11011101    // this is the value 14045

// << operator x << 2
	  x:  00011010 11101011
---------------------------
shifted:  01101011 10101100    // this is the value 27564

// >> operator, y >> 4
	  y:  00101100 00110110
---------------------------
shifted:  00000010 11000011    // this is the value 707

// ~ operator, ~x
	  x:  00011010 11101011
---------------------------
     ~x:  11100101 00010100    // this is the value -6892
```