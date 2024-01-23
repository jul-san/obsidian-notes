## Converting from Decimal to Another Base (Algorithm)
- When using an algorithm, repetitive division or multiplication can be used 

- Assume in both cases that *val* is the value and *b* is the base
### Algorithm to Print Integer Portion (Left of Decimal)
```cpp
void convert_int_part(float val, int b) {
    int whole, i, n;
    char d[] = "0123456789abcdefghijklmnopqrstuvwxyz";
    whole = val;
    i = 0;
    do {
        d[i] = whole % b;
        whole /= b;
        i++;
    } while (whole != 0);
    for (i; i >= 0; i--)
        printf("%c", d[d[i]]);
    printf("\n");
}

int main(){
	convert_int_part(420.69, 10);
	return 0;
}

//output will be 420
```
### Algorithm to Print Fractional Portion (Right of Decimal)
```cpp
void convert_frac_part(float val, int b) {
    int whole, i;
    float frac;
    char digits[] = "0123456789abcdefghijklmnopqrstuvwxyz";
    whole = val;
    frac = val - whole;
    i = 0;
    while (frac != 0 && i < MAXFRACDIGITS) {
        frac *= b;
        whole = frac;
        frac -= whole;
        printf("%c", digits[whole]);
        i++;
    }
    printf("\n");
}

int main(){
	convert_frac_part(420.69, 10);
	return 0;
}

//output will be 69, assuming MAXFRACDIGITS = 2
```

---
## Converting from Decimal to Another Base (Operation)
- The concept of repetitive division is used here, just without code

### Example: Convert  $13.25_{10}$ to binary
- To accomplish this, you must split the number into integer (left of decimal) and fractional (right of decimal)
$$13.25_{10} \rightarrow 13_{10} \text{, } 25_{10}$$
- Now conduct repeated division in the wanted base number (binary = 2) until quotient is 0

| Operation | Quotient | Remainder |
| --------- | -------- | --------- |
| 13/2      | 6        | 1         |
| 6/2       | 3        | 0         |
| 3/2       | 1        | 1         |
| 1/2       | 0        | 1         |
**Set the remainder in reverse order ONLY for integer portion!**
- Integer portion ($13_{10}$) is equal to 1101

- Conduct repeated multiplication

| Operation | Result | Integer | Fraction |
| --------- | ------ | ------- | -------- |
| 0.250 * 2 | 0.50   | 0       | 0.50     |
| 0.500 * 2 | 1.00   | 1       | 0.00     |
**Remainder can be set in normal order**
- Fractional portion ($25_{10}$) is equal to 01

$$\text{Therefore} \ 13.25_{10} \text{ is } 1101.01_{2}$$

---
## Converting Between Power of Two Bases
- Convert a value from one power of two base to another by **converting to binary** and **grouping bits**

### Example: Binary to Hexadecimal
$$\text{Given } 01010111011001_2$$
$$\text{Group the bits => } 0001_2 \ 0101_2 \ 1101_2 \ 1001_2$$
$$\text{Convert to Hexadecimal => } 1_{16} \ 5_{16} \ d_{16} \ 9_{16}$$
$$\text{Combine => } 15d9_{16}$$
$$\text{Therefore, } 01010111011001_2 \text{ is } 15d9_{16} \text{ in hexadecimal}$$
### Example: Binary to Octal
$$\text{Given } 11001111001_2$$
$$\text{Group the bits => } 011_2 \ 001_2 \ 111_2 \ 001_2$$
$$\text{Convert to Octal => } 3_{8} \ 1_{8} \ 7_{8} \ 1_{8}$$
$$\text{Combine => } 3171_{8}$$
$$\text{Therefore, } 11001111001_2 \text{ is } 3171_{8} \text{ in octal}$$
### Example: Hexadecimal to Octal
$$\text{Given } f5e71c_2$$
$$\text{Convert to Binary and Group into 4  => } 1111_2 \ 0101_2 \ 1110_2 \ 0111_2 \ 0001_2 \ 1100_2$$
$$\text{Group into 3  => } 111_2 \ 101_2 \ 011_2 \ 110_2 \ 011_2 \ 100_2 \ 011_2 \ 100_2$$
$$\text{Convert to Octal => } 7_{8} \ 5_{8} \ 3_{8} \ 6_{8} \ 3_{8} \ 4_{8} \ 3_{8} \ 4_{8}$$
$$\text{Combine => } 75363434_{8}$$
$$\text{Therefore, } f5e71c_2 \text{ is } 75363434_{8} \text{ in octal}$$
### Example: Octal to Hexadecimal
$$\text{Given } 60741_8$$
$$\text{Convert to Binary and Group into 3  => } 1111_2 \ 0101_2 \ 1110_2 \ 0111_2 \ 0001_2 \ 1100_2$$
---
## Integer Binary Representations
### Word Size
- *Word* represents the natural unit of data used by a processor
- Size determines number of integer values that can be represented
- Can also determine the range of addresses that can be accessed

### Unsigned Integers
- Corresponds to the integral portion of a weighted base 2 representation
- Binary representation with *n* bits has a possible range of values from 0 to $2^n - 1$

### Unsigned Representation in Different Sizes
| C Type             | Number of Bits | Range (decimal)                 |
| ------------------ | -------------- | ------------------------------- |
| unsigned char      | 8              | 0 to 255                        |
| unsigned short     | 16             | 0 to 65,535                     |
| unsigned int       | 32             | 0 to 4,294,967,295              |
| unsigned long long | 64             | 0 to 18,446,744,073,709,551,615 |
| general            | *n*            | 0 to $2^n -1$                   |

### Extending to a Larger Unsigned Representation
- Known as "zero extension"
- Fill in the new bits of the larger representation with zero

| C Type         | Number                           | Decimal |
| -------------- | -------------------------------- | ------- |
| unsigned char  | 10010110                         | 150     |
| unsigned short | 0000000010010110                 | 150     |
| unsigned int   | 00000000000000000000000010010110 | 150     |

### Binary Addition
- Corresponding binary digits are added from right to left with carries
![hello]()'https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2F1kcAq.png&f=1&nofb=1&ipt=6b28faf2f48be141c335572f6a6a3f7f6f56b218e31ea58d927196a4c4e49948&ipo=images'
### Two's Complement Representation
- The form of a negative binary number is the bitwise complement plus one
- Advantages: 
	- Only one representation of zero
	- Addition is straightforward
- Negation is slightly more complex
- Range of values in an *n*-bit two's complement is from $-2^{n-1}$ to $+(2^{n-1}-1)$

### Two's Complement Representations in Different Sizes
| C Type    | Number of Bits | Range (Decimal)                                         |
| --------- | -------------- | ------------------------------------------------------- |
| char      | 8              | -128 to 127                                             |
| short     | 16             | -32768 to 32767                                         |
| int       | 32             | -2,147,483,648 to 2,147,483,647                         |
| long long | 64             | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| general   | *n*            | $-2^{n-1} \text{ to } 2^{n-1}-1$                        |

### Two's Complement Negation
- Invert the bits and add 1 to negate two's complement
#### Example 1:

$$3_{10} = 00000000000000000000000000000011_2$$
$$-3_{10} = 11111111111111111111111111111100_2 + 1_2$$
$$= 11111111111111111111111111111101_2$$
$$= -3_{10}$$
#### Example 2:
$$-3_{10} = 11111111111111111111111111111101_2$$
$$3_{10} = 00000000000000000000000000000010_2 + 1_2$$
$$ = 00000000000000000000000000000011_2$$
$$= 3_{10}$$
### Subtraction by Negating and Adding
- $x-y=x+(-y)$
- This method helps to simplify hardware

#### Example: 25-6
 00000000000000000000000000011001
- 00000000000000000000000000000110


### Extending to a Larger Two's Complement Representation
- Known as sign extension
- Take the most significant bit from the value in the smaller representation
- Replicate that number to fill in the new bits
- Basically if positive, use 0's and if negative, use 1's

| C Type | Number                           | Decimal |
| ------ | -------------------------------- | ------- |
| char   | 00000011                         | 3       |
| short  | 0000000000000011                 | 3       |
| int    | 00000000000000000000000000000011 | 3       |
| char   | 11111101                         | -3      |
| short  | 1111111111111101                 | -3      |
| int    | 11111111111111111111111111111101 | -3      |

### Detecting Overflow
- Overflow occurs when result of an arithmetic operation is not in range of representable values
- In addition, this happens when the most significant bit of the operands are the same and the most significant bit of the result differs
- Basically, if you were to add to numbers in binary and the result doesn't match if you convert the result in decimal, than there is an overflow
---
## Floating Point Representations

### Scientific Notation
- Uses 3 integers to represent values:
	- radix (or base) *r*
	- significand (or mantissa) *s*
	- exponent *x*
- Standard form:
	- $s*r^x$

### Representing Floating-Point Values
- Representing floating-point values in a computer using uses 3 parts:
	- sign, indicates negative or positive
	- significand, contains bits in the value
	- exponent, power to which the significand is raised
- Can be calculated as follows:
$$(-1)^{Sign}*Significand*2^{Exponent}$$

### Normalized Floating-Point Values
- Normalized when there is a single bit set to the left of the radix point and there are no leading zeroes
- Can help maximize the number of values that can be represented
#### Example: 9.5
$$9.5_{10}=1001.1_2$$
$$=1*1001.1_2*8$$
$$=(-1)^0*1001.1_2*2^3$$











## IEEE 754 Floating-Point Standard

| Significant Bit | Exponent | Bits of the significand |
| --------------- | -------- | ----------------------- |
| 1 bit           | 8 bits   | 23 bits                 |



