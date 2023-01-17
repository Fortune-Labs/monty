# 0x19. C - Stacks, Queues - LIFO, FIFO

## Learning Objectives
At the end of this project, we learnt Stacks and Queues in C.

## Description

### The Monty language
Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

#### Monty byte code files

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

## Environment

Ubuntu 20.04 LTS via .....

## General
* What do LIFO and FIFO mean
* What is a stack, and when to use it
* What is a queue, and when to use it
* What are the common implementations of stacks and queues
* What are the most common use cases of stacks and queues
* What is the proper way to use global variables

 ## Requirements project

-  Allowed editors: vi, vim, emacs
-   All your files will be compiled on Ubuntu 14.04 LTS
-   SimpleYour programs and functions will be compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic
-   SimpleAll your files should end with a new line
-   A README.md file, at the root of the folder of the project is mandatory
-   SimpleYour code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
-   You allowed to use a maximum of one global variable
-   No more than 5 functions per file
-   You are allowed to use the C standard library
-   AThe prototypes of all your functions should be included in your header file called monty.h
-   Don’t forget to push your header file
-   YouAll your header files should be include guarded
-   You are expected to do the tasks in the order shown in the project

## Instruction given:
* To use the following data structures for this project, and to also include them in the header file.
```
/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
        int n;
        struct stack_s *prev;
        struct stack_s *next;
} stack_t;
```
```
/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
        char *opcode;
        void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;
```


## Tasks

### 0. push, pall
-   SimpleImplement the push and pall opcodes.
-   The push opcode
-   The opcode push pushes an element to the stack.

### 1. pint
-  Implement the pint opcode.
-   The pint opcode
-   The opcode pint prints the value at the top of the stack, followed by a new line.

### 2. pop
-   Implement the pop opcode.
-   The pop opcode
-   The opcode pop removes the top element of the stack

### 3. swap
-   Implement the swap opcode.
-   The swap opcode
-   The opcode swap swaps the top two elements of the stack.

### 4. add
-   SimpleImplement the add opcode.
-   The add opcode
-   The opcode add adds the top two elements of the stack.

### 5. nop
-   Implement the nop opcode.
-   The nop opcode
-   The opcode nop doesn’t do anything.

### 6. sub
-   Implement the sub opcode.
-   The sub opcode
-   The opcode sub subtracts the top element of the stack from the second top element of the stack.

### 7. div
-   Implement the div opcode.
-   The div opcode
-   The opcode div divides the second top element of the stack by the top element of the stack.

### 8. mul
-   Implement the mul opcode.
-   The mul opcode
-   The opcode mul multiplies the second top element of the stack with the top element of the stack.

### 9. mod
-   Implement the mod opcode.
-   The mod opcode
-   The opcode mod computes the rest of the division of the second top element of the stack by the top element of the stack.

### 10. comments
-   ImplementEvery good language comes with the capability of commenting. When the first non-space character of a line is #, treat this line as a comment (don’t do anything).

### 11. pchar
-   Implement the pchar opcode.
-   The pchar opcode
-   The opcode pchar prints the char at the top of the stack, followed by a new line.

### 12. pstr #advanced
-   TheImplement the pstr opcode.
-   The pstr opcode
-   The opcode pstr prints the string starting at the top of the stack, followed by a new line.

### 13. rotl #advanced
-   TheImplement the rotl opcode.
-   The rotl opcode
-   The opcode rotl rotates the stack to the top.

### 14. rotr
-   Implement the rotr opcode.
-   The rotr opcode
-   The opcode rotr rotates the stack to the bottom.

## Authors

* **Fortunatus Wulnye** - [Fortune-Labs](https://github.com/Fortune-Labs)

* **Simon Asakipaam** - [Asakippam-Simon](https://github.com/Asakippam-Simon)