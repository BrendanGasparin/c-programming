# Bits, Bytes, and Binary: Number Systems and Data Representation in Computer Science

Computers only understand electricty, which can be expressed as zeroes and ones: voltage or no voltage. All data in a computer is represented by zeroes and ones. In this chapter we will learn how zeroes and ones can be used to express human-readable decimal numbers, as well as other things like alphabetical characters, text strings, images, audio, and video.  

## Number Systems: Unary, Binary, Decimal, Hexadecimal, and Octal

There are many number systems for representing values in the world of mathematics. Humans tend to count using unary (base-1), and write numerals in decimal (base-10). Computers only know binary (base-2). So how do we represent decimal numbers and things like text programming statements in binary?  

WWe will take some time to explore different number systems so we can understand how data is represented in computers, and in the C programming language.  

### The Unary System (Base-1)

To understand binary, we will first look at the unary system.  

The unary system (also known as base-1) is the number system people use when they count on their hands, or tally with marks. It is the simplest way of representing numbers.  

Instead of using place values like decimal or binary, unary represents numbers by repeating a single symbol, e.g. fingers, or tally marks.   

![A diagram of the unary numbering system showing fingers and tally marks numbering one to five.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-001-unary.png)

Each digit represents an increment in the value of the number. For example, one finger usually means one, two fingers means two, three fingers means three, etc.  

This is called base-1 because there is only one symbol used to represent numbers (i.e. a finger, tally mark, etc.).  

With the unary system, five digits can count five numbers.  

What if there was a more efficient way to use these digits. For example, what if we weighted the value of a digit based on its position?  

### The Binary System (Base-2)

Binary (or base-2) is another number system: the number system used by computers. Binary is comprised of bits, which stands for binary digit. "Bi" implies two, and there are only two binary digits: zero and one.

In a computer, these are often represented by electicity, or an absence of electricity (e.g. in an electronic component or connection). So as well as representing zero and one, binary can be used to represent on versus off states, truth versus falsity, or any other binary decision.  

Multiple binary digits can be used to create a binary word. The length of this word is the number of binary digits it contains. Five binary digits is a 5-bit word.  

Binary is a positional number system, which means that the position of a bit in a pattern of bits affects it final value.

Let's look at a binary word of 5 bits, similar conceptually to a human hand, and see how many values we can represent with only five binary digits.  

The number zero can be represented with all zeroes.  

![Zero represented as a 5-bit binary word](../../assets/diagrams/chapter-03/itcp-diagram-ch03-002-binary.png)

If a bit in a binary number is zero, then its value is zero, regardless of its place. So `00000` has a value of `0`.  

The rightmost digit in a binary number (which we call the first digit) has a **place value** of `1`. If this bit is set to `1`, then we add the place value of the digit to the final value of the binary number. So, in a 5-bit binary word, the number `1` is represented as `00001`.  

![One represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-003-binary-1.png)

The second digit from the right has a **place value** of `2`. Therefore, to represent the value `2` in an 8-bit binary word, we set all the other digits to zero, and the second digit (from the right) to one.  

![Two represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-004-binary-2.png)

So the value of a binary digit is determined by its position in the binary number. The first digit has a place value of `1`, and the second digit has a place value of `2`.  

How do we represent the number `3`?

`3` is represented by turning on the right-most digit (which has a place value of `1`) and the second digit from the right (which has a place value of two). The values of these digits are added together to get 3.  

![Three represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-005-binary-3.png)

To determine the value of a binary number with more than one `1` bit, we can simply add the place values of those `1` bits together.  

But how do we know what the place values are without being told. The first place value (from the right) is `1`. The second is `2`.

The place value of the third digit is `4`, so to represent `4` in binary we can set all the other columns to zero and set the third digit to 1.  

![Four represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-006-binary-4.png)

Note that this is similar to "carrying" a number in decimal mathematics. We incrememnt a new digit and set all the ones to its right back to zero.  

To get `5` we keep the third digit as one and also change the first digit to one. Four plus one equals five, so the final value equals five.  

![Five represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-006-binary-4.png)

Six is a combination of ones in the places valued `4` and `2`, because `4 + 2 = 6`.  

![Six represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-008-binary-6.png)

Seven is all three of the first three bits set to one: `00111`.  These are multiplied by their place values and added together to equal `7`.  

![Seven represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-009-binary-7.png)

If we want to represent a higher number, we need to use an additional bit. Once more, we would carry the three rightmost bits of `00111`, flipping them to zero, and setting the fourth bit to one.  

![Eight represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-010-binary-8.png)

So it takes three digits to represent eight values, from `0` to `7`. In unary, this would take seven digits, or two hands.  

Using binary, how many values can we represent in five digits?  

You may have notices that the place value of each position doubles the further we move to the left. From this we can extrapolate the place value of the remaining position. The fifth digit has a place value of `16`.  

![Thirty one represented as a 5-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-011-binary-31.png)  

In binary, we can represent 32 values with five digits (from zero to thirty one). A binary number can represent as many values as `2^n` where n is the number of bits.  

How does this work? As we have already stated, the position of each digit affects the value of the number that it represents.  

The bit in each each place is multiplied by the place value for that position, and then these products are added together to give the final value. In this way we can represent any integer by combining enough bits.  

![Sixty seven represented as an 8-bit binary word.](../../assets/diagrams/chapter-03/itcp-diagram-ch03-012-binary-67.png)

Bits can be represented in a computer with electricity. For example, a zero might be represented by zero voltage, and one represented by 5 volts.  

Binary can then be stored in the charges of transistors. These are like switches than can be turned on or off by capturing or discharging electricity. A transistor storing no electricity equals zero. A transistor storing electricity equals one. Modern computers contain millions of transistors, allowing them to work with a lot of large binary values.  

Binary can also be transmitted through connections like wires in the form of pulses of electricity as well.  

Binary is used in computers because it translates so well to the world of electronics.  

Humans do not use binary in written mathematics. They use the decimal number system. "Dec" implies 10 and the decimal number system has 10 digits, `0` through `9`. But it turns out that the decimal system and binary have a lot in common.  

### The Decimal Number System (Base-10)

Much as computer languages work in the same way as human languages, the computer's number of system of binary (base-2) essentially works the same way as the numerical system most humans use: the decimal number system (base-10).  These number systems are not arbitrary. They have mathematical relationships that mean you can translate numbers between them.  

Decimal is the written number system most of us are familiar with, with ten numeric symbols ranging from `0` to `9`. Like binary, decimal is a positional system. The position of the digit affects its total value.  

You may rmember learning about this in your childhood. In the number `42`, the rightmost digit has a value of `2`, but the second digit to the right, the `4`, has a value of `4 * 10`. This is because, in elementary school mathematics, the first column on the right is a "ones" column and the next column to the left is the "tens" column.  

Similarly, in the number `187`, the `1` had a value of `100`, because it is in the "hundreds" column, the third from the right.  

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
