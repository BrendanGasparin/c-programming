# 2. The Funadmentals of Computing: Hardware, Software, and Operating Systems  

In order to truly understand programming in the C language we need to understand the fundamentals of computing: hardware, software, and operating systems.  

## Hardware and Software  

A computer is comprised of hardware and software.  

Hardware is the physical, tangible components of a computer. This might include the case and any circuit boards, chips, wires, or other components and connections inside it, as well as external devices like keyboards and monitors. If you can physically touch it then it is hardware.  

Software is programs and data: information stored in some format.  

A program is a series of instructions, as we have discussed.

Data is the raw information that a program manipulates. These are represented in binary numbers (zeroes and ones) which we will discuss in a future chapter, but binary numbers can also be used to represent human-readable numbers, text, images, sound, video, and anything else that mathematics can possibly represent.  

A computer requires both hardware and software to operate. The hardware can add one plus one, but only if software (i.e. a program) tells it to do so. Without software, a computer is just an inert bundle of physical components. Without hardware, software is just a series of instructions with nothing to execute them.  

## Hardware  
In order to be useful and perform mathematical operations on data, a modern computer needs the following hardware components:  

- Central processing unit (CPU)  
- Main memory  
- Secondary memory  
- Input and output devices  
- Connections between components  

### Hardware: The Central Processing Unit (CPU)  
The component that executes program instructions is called a processor, or microprocessor. In a modern computer, this is a silicon chip. There are many different types of processors. Some are for general use, some specialise in numerical mathematics, and others specialise in graphical operations.  

Computers generally have one or more processors, but conceptually (and historically) a computer has a single central processing unit (also called a CPU) that executes program instructions.  

Processors can perform mathematical operations and make logical decisions.  

The CPU is continually running through the fetch-decode-execute cycle.

In this cycle it:  

1. Fetches the next programming instruction from main memory
2. Decodes the instruction from binary to determine the instruction
3. Execute the instruction, accessing and modifying data from the main memory if instructed
4. Back to step 1 to fetch the next instruction

### Hardware: Main Memory  
The main memory of a computer is also called primary storage. This is an area to store programs and data that are being actively used. Main memory in modern computers are usually RAM, which stands for random access memory.  

In this way, the functionality of a computer is split in two. The main memory holds most of the data and program instructions that a program needs. The CPU requests data from main memory when needed, performs operations on it, and writes the results of those operations back to main memory.  

Main memory stores information as electricity in RAM chips. When a computer is powered off, the RAM loses electricity and forgets all of the information that was stored. Main memory is volatile: when a computer loses power, the main memory loses all of its stored information.  

If we want to retain information when a computer is rebooted, we need another type of memory.  

### Hardware: Secondary Memory (or Secondary Storage)  
Secondary memory is long-term storage. It is not volatile, and the data it holds can survive losing power.  

There are many types of secondary memory: hard drives, USB drives, optical disks, and older technology like floppy disks, magnetic tape, and even punch cards.  

Modern computers have one or more types of internal secondary memory to hold things like the operating system, software applications, and data.  

When main memory requires information for the CPU to process, it reads the information from secondary memory. The processor can then read the data from main memory, perform operations on it, and write the results of those operations back to main memory. If these results need to be stored long term, they can then be written back to secondary memory, at which point they can be safely discarded from main memory.

### Hardware: Input and Output Devices  
As we discussed in chapter 1, for a computer to be useful there needs to be a way to input information into it, and a way for it to output information. This is what input and output devices are for.  

Input devices like a keyboard, mouse, or sensor can be used for humans to input information into a computer. Output devices like monitors and speakers can be used by the computer to display output.  

Some input and output devices are less obvious. A camera is an input device, as is a barcode scanner connected to a digital cash register. A printer is an output device, as are the "stop" and "go" lights at a traffic intersection.  

### Hardware Connections  
The CPU must connect directly to the main memory for a computer to quickly read, write, and process data. There must also be a way for primary memory to write and read information to and from secondary memory.
