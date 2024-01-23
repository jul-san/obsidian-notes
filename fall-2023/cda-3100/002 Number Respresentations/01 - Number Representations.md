## Weighted Positional Notation
- The position of a number indicates its value
- The sum of _**n**_ digits to the left of the decimal and _**m**_ digits to the right is the **weighted sum**

$$
	\text{Weighted Sum = }\sum\limits_{i=-m}^{n-1}d_i \cdot base^i, 
	\text{ where } d = digit \text{ and } i = index
$$
### Example:
![Positional Notation | 400](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwikiwandv2-19431.kxcdn.com%2F_next%2Fimage%3Furl%3Dhttps%3A%252F%252Fupload.wikimedia.org%252Fwikipedia%252Fcommons%252Fthumb%252F7%252F78%252FPositional_notation_glossary-en.svg%252F1500px-Positional_notation_glossary-en.svg.png%26w%3D2048%26q%3D50&f=1&nofb=1&ipt=9ee13439be5d1a8ac7860b0094b69f7960e7713450bd56dbb28a52bd02449256&ipo=images)

- Given that the base (radix) is 10, we can use the formula to find the weighted sum:
$$
1125.0 = (1 \cdot10^3)+(1 \cdot10^2)+(2 \cdot10^1)+(5 \cdot10^0)+(0 \cdot 10^{-1})
$$
---
## Common Bases
| Base | Name        | Digits   |
| ---- | ----------- | -------- |
| 10   | Decimal     | 0-9      |
| 2    | Binary      | 0-1      |
| 8    | Octal       | 0-7      |
| 16   | Hexadecimal | 0-9, a-f |

---
## Range of Values
- The number of unique values can be formed a sequence can digits can be represented by:
$$M^N \ where \ M \text{ is the base and } \ N \text{ is number of digits}$$
### Example:
- Using base 10, what number of values can be represented with a 3 digit number?

$$\text{Using } M^N \text{, plug in 10 for } M \text{ and 3 for } N$$
$$ 10^3 \ = \ 1000$$
$$\text{Therefore, we can conclude that there are 1000 values in the range of [0, 999] that can be represented}$$
___
## Binary Representations
- Binary digit is referred to as a __bit__
- Sequence of bits can have different data values based on interpretation
	- unsigned integers
	- signed integers
	- floating-point
	- characters
- Sequence can also represent machine instructions
