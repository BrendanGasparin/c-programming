# 1. Introduction to Programming (Using the C Programming Language)  

Welcome to this introduction to programming using the C programming language!  

This book aims to teach you the art and science of writing computer programs.  

This will involve learning to think logically and creatively, solving problems systematically and efficiently, and writing code that is correct, efficient, and well-designed.  

We are going to learn using the C programming language, a relatively old computer language that still underlies the operations of many modern systems today.  

The C language is popular and relevant in the modern world and is ideal for teaching the low level fundamentals of programming that can be abstracted away by more modern languages.  

Are you ready to learn one of the most powerful skills you can master in the modern world? Let's go!  

## What is Computer Programming?  

A computer is anything that performs computations. Computations are mathematical or logical operations. This means that if you can count or make decisions based on logic, you are technically a computer. In fact, before the digital age, the term "computer" was generally used to refer to humans that were good at mathematics.  

Of course, nowadays, and for our purposes, a computer is assumed to be a digital device that can perform computations.  

A computer program is a set or sequence of instructions for a computer to perform. Programming is the act of writing a computer program, and one who does so is a programmer.  

What can programming do? Just think of all of the uses computer technology has in the modern world!  

When people think of software they might think of their smartphone apps, or their laptop computer programs, or maybe even a workplace productivity tool or two. But information technology is deeply ingrained into the fabric of our world.  

Almost every aspect of human endeavour nowadays is catalogued and managed with vast databases of information and the software designed to manage them. Data drives every day life: your life, your bank account, your taxes, business, educational and medical institutions all collect massive amounts of data that must be stored and manipulated by computers programs. Computers (and computer programs) are used to further every science and industry, every frontier of human knowledge.  

Programmers build systems that run governments and Fortune 500 companies, control city utility grids, and send rockets into space. They write and maintain the code that keeps modern society and its many complex moving parts interlocked and functioning.  

In order to be useful in the real world, a computer (and a computer program) must be able to accept input from the outside world, and must be able to output the result of its computations on that input.  

This essentially makes a computer program a black box with input going in one end and output coming out of the other.  

![Program diagram with input in and out.](../../assets/diagrams/chapter-01/itp-diagram-ch01-001.png)  

Obfuscated inside the box is whatever algorithm, problem-solving processes, and computations the programmer implemented when they wrote the program. These are applied to the input to give an output. For example, and electronic cash register might be programmed to sum the scanned items being purchased by a customer. A computer game takes input from the controller, applies it to the player's character in the game, and then outputs the result on the screen and speakers.  

A program is correct if it produces the expected and correct output for all inputs.  

## Why Learn Programming?  

Programming is not just about building apps and launching rockets. It is also about learning to think clearly and logically, to solve problems systematically and efficiently, and to express function and creativity through code.  

Programming teaches you to:  

- Think systematically and effectively  
- Break complex problems into smaller parts  
- Design step-by-step solutions  
- Value efficiency and economy  
- Diagnose and debug issues  

## The C Language: The Best First Language to Learn  

Ultimately, once you have learned the fundamentals of programming in the C language, you will be able to apply what you have learned to other computer languages and pick them up very quickly.

## What This Book Will Teach You  

## Hello, World: The First C Program  

The first program a programmer writes is traditionally a "hello, world" program. This is one of the simplest programs that can be written in C. It simply prints the words "hello, world" to the screen.  

```C
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```
