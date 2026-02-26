# Bits, Bytes, and Binary: Number Systems and Data Representation in Computer Science

Computers only understand electricty, which can be expressed as zeroes and ones: voltage or no voltage. All data in a computer is represented by zeroes and ones. In this chapter we will learn how zeroes and ones can be used to express human-readable decimal numbers, as well as other things like alphabetical characters, text strings, images, audio, and video.  

## Number Systems: Unary, Binary, Decimal, Hexadecimal, and Octal

There are many number systems for representing values in the world of mathematics. Humans tend to count using unary (base-1), and write numerals in decimal (base-10). We will take some time to explore different number systems so we can understand how data is represented in computers, and in the C programming language.  

### The Unary System (Base-1)

The unary system (also known as base-1) is the number system people use on their hands, or when they tally. Each digit represents an increment in the value of the number. For example, one finger extended usually means one, two fingers extended means two, three fingers extended means three, etc.  

This is called base-1 because there is only one possible digit (i.e. a finger, tally mark, etc.).  

### The Binary System (Base-2)

Binary (or base-2) is another number system: the number system used by computers. Binary is comprised of bits, which stands for binary digit. "Bi" implies two, and there are only two binary digits: zero and one.  

Binary is a positional number system, which means that the position of a bit in a pattern of bits defines its possible value. In comparison, unary is a non-positional number system. The position of the digits (or tally marks) does not matter. Each digit is one increment, regardless of position.  

But in a binary word (e.g. an 8-bit byte), the position of each digit affects the value represented by that digit. In this way, the number zero can be represented by a zero, or all zeroes. e.g. 

`00000000₂`  

Note that the subscript `₂` at the end of the number indicates that it is a binary number. This is used to differentiate it from decimal numbers and is not actually a digit or part of the final value.  

The right-most digit in a binary number represents the value `1`. So, in an 8-bit binary word, the number `1` can be represented as:  

`00000001₂`  

The second digit from the right represents the value `2`. To represent the number `2` in an 8-bit binary word we set all the other digits to zero, and the second digit from the right to one.

`00000010₂`  

Three is represented by turning on the right-most digit (representing one) and the second digit from the right (which represents two). The values of these digits are added together to get 3.  

`00000011₂`  

The value of the third digit from the right is 4, so to represent 4 we need only set this digit to 1.  

`00000100₂`  

And to get five we keep this digit as one, but also change the rightmost digit to one. Four plus one equals five.  

`00000101₂`  

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
