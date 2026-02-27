# Bits, Bytes, and Binary: Number Systems and Data Representation in Computer Science

Computers only understand electricty, which can be expressed as zeroes and ones: voltage or no voltage. All data in a computer is represented by zeroes and ones. In this chapter we will learn how zeroes and ones can be used to express human-readable decimal numbers, as well as other things like alphabetical characters, text strings, images, audio, and video.  

## Number Systems: Unary, Binary, Decimal, Hexadecimal, and Octal

There are many number systems for representing values in the world of mathematics. Humans tend to count using unary (base-1), and write numerals in decimal (base-10). Computers only know binary (base-2). So how do we represent decimal numbers and things like text programming statements in binary?  

WWe will take some time to explore different number systems so we can understand how data is represented in computers, and in the C programming language.  

### The Unary System (Base-1)

The unary system (also known as base-1) is the number system people use when they count on their hands, or tally with marks.  

![A diagram of the unary numbering system showing fingers and tally marks numbering one to five.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-001-unary.png)

Each digit represents an increment in the value of the number. For example, one finger extended usually means one, two fingers extended means two, three fingers extended means three, etc.  

This is called base-1 because there is only one possible digit (i.e. a finger, tally mark, etc.).  

With the unary system, five digits can count five numbers.  

What if there was a more efficient way to use these digits. For example, what if weighted the value of a digit based on its position?  

### The Binary System (Base-2)

Binary (or base-2) is another number system: the number system used by computers. Binary is comprised of bits, which stands for binary digit. "Bi" implies two, and there are only two binary digits: zero and one. In a computer, these are often represented by electicity, or an absence of electricity (e.g. in an electronic component or connection).  

Binary is a positional number system, which means that the position of a bit in a pattern of bits affects it final value. Let us take a binary value of 5 bits (i.e. binary digits).  

The number zero can be represented by a zero, or all zeroes.  

![Zero represented as a 5-bit binary word](../../assets/diagrams/chapter-03/itcp-diagram-ch03-002-binary.png)

None of the digits are one, so their positions are not important. The value they each represent is multiplied by zero, so the whole binary word equals zero.  

The right-most digit in a binary number (which we call the first digit) represents the value `1`. This is its **place value**. So, in a 5-bit binary word, the number `1` can be represented as `00000001`.  

![One represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-003-binary-1.png)

The second digit from the right represents the value `2`. Therefore, to represent the value `2` in an 8-bit binary word, we set all the other digits to zero, and the second digit (from the right) to one. This is because `2` is the **place value** of the second digit.  

![Two represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-004-binary-2.png)

Three is represented by turning on the right-most digit (representing one) and the second digit from the right (which represents two). The values of these digits are added together to get 3.  

![Three represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-005-binary-3.png)

The **place value** of the third digit (from the right) is 4, so to represent `4` change the other columns to zero and set the third digit to 1.  

Note that this is similar to "carrying" a number in decimal mathmematics.  When we need to use a new digit to represent larger numbers we reset all the previous digits to zero and "carry" to the next digit.  

![Four represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-006-binary-4.png)

To get five we keep the third digit as one (because it has a place value of four) and also change the rightmost digit to one (because it has a place value of one). Four plus one equals five, so the final value equals five.  

![Five represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-006-binary-4.png)

Six is a combination of ones in the places valued `4` and `2`, i.e. `00101`.  

![Six represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-008-binary-6.png)

Seven is all three of the first three bits set to one: `00111`.  These are multiplied by their place values and added together to equal `7`.  

![Seven represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-009-binary-7.png)

If we want to represent a higher number, we need to use an additional bit. Once more, we would set the rightmost bits of `00111` to zero and set the next bit to the left as one.  

![Eight represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-010-binary-8.png)

So it takes three digits to represent eight values, from `0` to `7`. In unary, this would take seven digits, or two hands.  

Using binary, how many values can we represent in five digits?  

You may have notices that the place value of each position doubles the further we move to the left. From this we can extrapolate the place values of the remaining positions.  

![Thirty one represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-011-binary-31.png)  

How does this work? As we have already stated, the position of each digit affects the value of the number that it represents.  

The rightmost digit is multiplied by one. If the rightmost digit is a `1`, then `1 * 1 = 1`, so the value of that digit is one. If the rightmost digit is a `0`, then `0 * 1 = 0`, so the value of that digit is zero.  

The next digit to the left is multiplied by two. If it is a `1` then `1 * 2 = 2` so the value of that digit is two. Once again, if it is multiplied by zero then `0 * 2 = 0`, so the value of that digit is zero.  

The next digit to the left (the third digit) is multiplied by four. If it is a `1` then `1 * 4 = 4` so the value of that digit is four. the third digit is zero then `0 * 4 = 0` so the value is zero.  

When all the digits and their values are known, those with a digit of `1` can be added together for the final total. Those with a `0` can be discarded.  

You might notice that, in binary, the rightmost place is multiplied by one. For each place removed to its left, the digit's multiplier is doubled.  

As we have discussed, zeroes and ones can be represented in a computer with electricity. For example, a zero might be represented by zero voltage, with one represented by 5 volts.  

Binary can then be expressed in transistors. Modern computers contain millions of transistors. These are like switches than can be turned on or off by capturing or discharging electricity. A transistor with no electricity equals zero. A transistor with electricity equals one.  

### The Decimal Number System (Base-10)

Much as computer languages work in the same way as human languages, the computer's number of system of binary essentially works the same way as the numerical system most humans use: decimal.  

Decimal is the number system most of us are familiar with, with ten digits from `0` to `9`. Like binary, decimal is a positional system. The position of the digit affects its total value. For example, in the number `42`, the rightmost digit has a value of `2`, but the second digit to the right, the `4`, has a value of `4 * 10`, because it is in what elementary mathematics calls the "tens" column. Similarly, in the number `187`, the `1` had a value of `100`, because it is in the "hundreds" column, the third from the right.  

What is the pattern here? In each column from right to left we are multiplying the digit in that place by ten to the power of how many positions it is from the rightmost digit.  

The rightmost digit is multiplied by `10^0`, or `1`. The next digit to the left is multiplied by `10^1`, or `10`. The next digit to the left of that is multiplied by `10^2`, or `100`. We multiply by 10 because we are using base-10, which has a total of ten digits (`0` through `9`).  

### How to Calculate a Binary Number

Binary works exactly the same. But because we only have two digits, we multiply the bit in each position by `2` to the power of how many positions it is from the rightmost digit.  

This is why powers of `2` come up so much in computer science: hardware specifications, computer memory, hard disk space. For example, bits are normally managed in groups of eight. Eight bits are a byte.   

The more bits you have, the greater range of values you can represent. `n` bits can represent `2^n` values. Modern computers can use 32-bits (four bytes) to represent a range of about 4 billion integers (or 2 billion if you include negative integers). With 64-bit words (eight bytes) we can represent `2^64` values, which is quite a large number.  

For the sake of simplicity, we will look at 8-bit words.  


 
---

Note that if we have a value that is too large to be represented by a particular piece of memory, this might cause unexpected behaviour like rolling back to zero or overwriting memory that should not be overwritten.  

## Data Representation in Computer Science

If we want to express things with binary numbers then we need standardised methods to do so. This way, a program written on one computer will be compatible when run on similar computers.  
