TLMlang is a stack-based, two-dimensional programming language focused on meta programming.
Inspirations include Brainfuck, Befunge and cellular automata.

This repo is an interpreter for TLMlang writting in C#

# Specification
Below is the list of all key-"words" allowed in .tlm files:

| Instruction   | |
| - | - |
| U, D, L, R    | Redirect flow of instruction pointer (up, down, left, right)  |
| 0, 1, ..., 9  | Pushes the value of the cell to the stack  |
| P | pops the value on top of the stack and puts it in the current cell modulo 10 |
| L | pops the value on top of the stack and puts it in the current cell, interpreted as a letter, "modulo Z + 1" |
| R | pops the value on top of the stack and puts it in the four orthogonal neighbors |
| H | pops the value on top of the stack and puts it in the left and right neighbors |
| V | pops the value on top of the stack and puts it in the top and bottom neighbors |
| X | pops the value on top of the stack and puts it in the four diagonal neighbors |
| A | pops the value on top of the stack and puts it in all eight neighbors |
| S | pushes the sum of all eight neighbors to the stack after clearing the cells |
| M | pushes the product of all eight neighbors to the stack after clearing the cells |
| I | increments the value on top of the stack by 1 |
| D | decrements the value on top of the stack by 1 |
| O | redirects control flow to the right (or left) if the top value on the stack is zero (nonzero) |
| Z | halts the program and waits for user input in the form of a letter, puts that letter into the cell |
| Y | halts the program and waits for user input in the form of a number, puts that number into the cell |
