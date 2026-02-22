# 1. Introduction to Programming (Using the C Programming Language)  

Welcome to this introduction to programming using the C programming language!  

This book aims to teach you the art and science of writing computer programs.  

This will involve learning to think logically and creatively, solving problems systematically and efficiently, and writing code that is correct, efficient, and well-designed.  

We are going to learn to program using the C language, a relatively old computer language that still underlies the operations of most modern systems today.  

The C language is popular and relevant in the modern world and is ideal for teaching the low level fundamentals of programming that can be abstracted away by more modern languages.  

Are you ready to learn one of the most powerful skills you can master in the modern world? Let's go!  

## What is Computer Programming?  

A computer is anything that performs computations. Computations are mathematical or logical operations. This means that if you can count or make decisions based on logic, you are technically a computer. In fact, before the digital age, the term "computer" was generally used to refer to humans that were good at mathematics.  

Of course, nowadays, and for our purposes, a computer is assumed to be a digital device that can perform computations.  

A computer program is a set or sequence of instructions for a computer to perform. Programming is the act of writing a computer program, and one who does so is a programmer.  

In order to be useful in the real world, a computer (and most computer programs) must be able to accept input from the outside world for computation, and output the result of its computations in some way.  

This essentially makes a computer program a black box with input going in one end and output coming out the other.  

![Program diagram with input and output.](../../assets/diagrams/chapter-01/itp-diagram-ch01-001.png)  
*Figure 1: Program with input and output.*

Obfuscated inside the box is whatever algorithms, problem-solving processes, and computations the programmer implemented when they wrote the program. These are applied to the input to give an output.  

For example, an electronic cash register might be programmed to sum the scanned items being purchased by a customer. A computer game takes input from the controller, applies that input to the player's character in the game, and then outputs the result on the screen and speakers.  

A program is correct if it produces the expected and correct output for all inputs. Verifying this can often take extensive testing.  

Programming is a technical process, but also a creative one, like sculpting, painting, or music. Unlike formal science where we begin with a hypothesis and test or refine it until it can be proven, in computer science we begin with a goal or end in mind and then write code until we reach that goal or end.  

Programs are written in programming languages. This is also referred to as code (and programming as coding).  

## What is a Programming Language?  

A programming language specifies words and symbols that can be used for writing a program. It also defines rules for combining these words and symbols to form valid program statements. In this way, a computer language is much like a human language. Human languages also specify words, punctuation, and rules that can be used to form understandable sentences.  

## Source Code, Compilers, and Software Applicatons

Of course, computers do not understand human languages like English. They do not really understand programming languages like C either. Computers are ultimately electronics that only understand pulses of electricity. These can be expressed with binary values: on or off, electricity or no electricity, one or zero, true or false.  

You may have heard that computers only understand the mathematics of binary, a number system comprised entirely of zeroes and ones. This is true. Human-readable programming languages were written as an intermediary so that humans could read and write sensible commands for computers.  

Programmers tend to write in human-readable languages like C. This is called source code. It is usually stored in plain text files. Source code can be fed through programs called compilers and interpreters that convert the code into binary instructions for computers to execute.  

C source code contains one or more functions. A function contains one or more statements. In C, execution begins with a function called main(). If there is no main() function, the program will (?)  

This source code is then sent through a program called a C compiler than converts it into machine-readable binary instructions. The result is an executable file (also called a binary) that can br ran as a software application.  

To write a program in C we only have to understand the words and symbols used to write in the language, and the rules used to combine those into meaningful programming statements.

## Why Learn Programming?  

Programming is not just about building apps and launching rockets. It is also about learning to think clearly and logically, to solve problems systematically and efficiently, and to express function and creativity through code.  

There are plenty of reasons to learn programming. Here are seven.  

### 1. Programming Teaches You to Think Clearly

Programming teaches you to:  

- Think systematically, logically, and effectively
- Think in an organised and structured manner  
- Break complex problems into smaller parts  
- Design step-by-step solutions  
- Value efficiency, economy, and correctness  
- Diagnose and debug issues  

These skills can transfer into other areas, like business, school, or personal life.

### 2. Programming Gives You The Power to Build  

Programming is ultimately a creative discipline, like sculpting, painting, or making music. Unlike in scientific fields, where we create a hypothesis and then test and refine it until it matches the real world, programmers begin with an end in mind and write code until they have achieved their goal.  

If it is within the bounds of what computing accomplish, then you can create a program to accomplish it.

### 3. Programming Opens Career Opportunities  



### 4. Programming Enables Automation  

A lot of the power of programming is that it enables the automation of tasks that once had to be performed with human labour.  

### 5. Programming Helps You Understand the Modern World  

When people think of software they might think of their smartphone apps, or their laptop computer programs, or maybe even a workplace productivity tool. But information technology is deeply ingrained into the fabric of our world.  

Almost every aspect of human endeavour nowadays is catalogued and managed nowadays as vast databases of information. These are created and managed by programs written by programmers!  

Data drives every day life: your social security number, your identity, your bank account, your taxes, are all tracked in massive computer sysystems. Governments, militaries, academic instutions, the medical industry, private enterprises, and more all collect and process massive amounts of data that must be stored and manipulated by computers programs. Computers (and computer programs) are used to further every science and industry, every frontier of human knowledge.  

Programmers build systems that run empires, nations, and Fortune 500 companies. Their programs control city utility grids, global economic and logistical networks, and send rockets into space. Programmers write maintain the code that keeps modern society and its many complex moving parts interlocked and functioning.  

### 6. Programming Builds Resilience  

### 7. Programming is Foundational to Emerging Technologies  



## Why Learn C As Your First Language    

Ultimately, once you have learned the fundamentals of programming in the C language, you will be able to apply what you have learned to other computer languages and pick them up very quickly.

## What This Book Will Teach You  

This book will teach you to solve problems using computers and programming.

We will learn:

- Syntactic knowledge: The cynactics of the C programming language
- Conceptual knowledge: What we can do with computers and C, conceptually
- Strategic knowledge: Strategies for solving problems using programming  
- Documentation: How to properly document programs, processes, and software products  

## Hello, World: The First C Program  

The first program a programmer writes is traditionally a "hello, world" program. This is one of the simplest programs that can be written in C. It simply prints the words "hello, world" to the screen.  

Here is the source code.

```C
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");

    return 0;
}
```
