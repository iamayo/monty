# C - Stacks, Queues - LIFO, FIFO
| C | Group project | Algorithm | Data structure |
## Monty
> This is an introductory project that explains what LIFO and FIFO mean
> What a stack is, and when to use it what a queue is, and when to use it
> What are the common implementations of stacks and queues what are the
> most common use cases of stacks and queues, what is the proper way to
> use global variables, and how to work with git submodules.

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

## Monty Bytecode
Files containing Monty byte codes usually have the `.m` extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

```
 push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$

```

Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:

```
push 0 Push 0 onto the stack$
push 1 Push 1 onto the stack$
$
push 2$
  push 3$
                   pall    $
$
$
                           $
push 4$
$
    push 5    $
      push    6        $
$
pall This is the end of our program. Monty is awesome!$

```

## Usage

1. Fork (this will be a link to a guide to forking)
2. Clone (link as well)
3. Run the following command:
```
 gcc -Wall -Werror -Wextra -pedantic *.c -o monty.
```
4. To run files, commands take the following form:
```
./monty bytecode_file
```

## List of Files

## Operation Codes
These are the available Operation Codes:
| Opcode | Description |
| :----: | :---------- |
| push | Pushes an element to the stack. e.g (push 1 # pushes 1 into the stack) |
| pall | Prints all the values on the stack, starting from the to of the stack. |
| pint | Prints the value at the top of the stack. |
| pop | Removes the top element of the stack. |
| swap | Swaps the top two elements of the stack. |
| add | Adds the top two elements of the stack. The result is then stored in the second node, and the first node is removed. |
| nop | Doesn't do anything |
| sub | Subtracts the top element of the stack from the second top element of the stack. The result is then stored in the second node, and the first node is removed. |
| div | Divides the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed. |
| mul | Multiplies the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed. |
| mod | Computes the remainder of the top two elements of the stack from the second top element. The result is then stored in the second node, and the first node is removed. |
| # | When the first non-space character of a line is `#`, the line will be treated as a comment` |
| pchar | Prints the character at the top of the stack, followed by a new line. |
| pstr | Prints the integers stored in the stack as their ascii value representation. It stops printing when the value is 0, when the stack is over and when the value of the element is a non-ascii value. |
| rotl |  Rotates the top of the stack to the bottom of the stack. |
| rotr | Rotates the bottom of the stack to the top of the stack. |
| stack | This is the default behavior. Sets the format of the data into a stack (LIFO). |
| queue | Sets the format of the data into a queue (FIFO). |

### Authors
* [Ayo Afolabi](https://github.com/iamayo)
* [Ayomide Fagboyo](https://github.com/ayomidefagboyo)
