# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers
Please write your answers here

Q1: - b. A Unix-like operating system

Q2: - b. Linux

Q3: - d. simple

Q4: - b. As interrupts

Q5: - b. 256

Q6: - c. Sh

Q7: - a. Round-robin scheduling

Q8: - a. Paging

Q9: - d. Both b and c

Q10: - b. No

Q11: - c. MIT


Q12: 
1.UNUSED:- not being used (waiting to initialise or already terminated)
2.EMBRYO:- newly created and is still being set up (hardware allocation)
3.SLEEPING:- waiting for an event to occur (time passing,signal,or I/O operations)
4.RUNNABLE:- ready to execute but waiting for the CPU to be free
5.RUNNING:- executing on cpu
6.ZOMBIE:- completed execution - waiting for the parent to collect exit status before being terminated

   
Q13: The xv6 operating system implements a 6 layered file system. The lowest layer is responsible for writing/reading data from the secondary memory, whereas the highest layer provides interfaces to be used by other high level programs.

Q14: A system call is when the program makes a request to the kernel to directly access some memory or hardware resources, or get some other information about the system. A library call means using a function which is provided by some library. The functions might invoke some system calls, but a programmer interacts with the abstracted library function only. For example, **fork()** is a system call, whereas **printf() (or cprintf() )** is a library call.

Q15: In xv6, paging is used for memory management. xv6 uses 32 bit VA, so memory size can go upto 4GB. A page size of 4KB is maintained, and a 2 level page table is used. Paging helps in non-contiguous memory allocation, by dividing memory into frames and programs into pages of equal sizes.

Q16: Three shell commands:
   1. ls - shows files in a directory
   2. echo - prints on shell
   3. grep - find some text in file

Q17: In xv6, the process synchronisation occurs with the help of locks. It is essential to have a process synchronization mechanism so that memory consistency can be maintained by avoiding race conditions etc, and to avoid deadlock conditions. 

Q18: When an interrupt occurs, the processor execution of current program is stopped and an interrupt handler begins execution. This handler is responsible for dealing and resolving the interrupt. Once this is over, the program again starts (if it has not been terminated). Its register values are saved at the time of interrupt, so that these can be restored at this instant.

Q19: xv6 has no implementation of a virtual memory.

Q20: 
