# **0x19. C - STACKS, QUEUES - LIFO, FIFO**
`C` `Group project` `Algorithm` `Data structure`

# Resources
- [Google](https://www.google.com/webhp?q=stack%20and%20queue)
- [How do I use extern to share variables between source files in C?](https://stackoverflow.com/questions/1433204/how-do-i-use-extern-to-share-variables-between-source-files)
- [Stacks and Queues in C](https://data-flair.training/blogs/stacks-and-queues-in-c/)
- [Stack operations](https://www.digitalocean.com/community/tutorials/stack-in-c)
- [Queue operations](https://www.edureka.co/blog/queue-in-c/)

<!-- man or help:
- `` -->

# Learning Objectives
<details>
<summary><h3>What do LIFO and FIFO mean</h3></summary>

In C, LIFO and FIFO are terms often used in the context of data structures, particularly stacks and queues, to describe the order in which elements are accessed or removed from the data structure.

1. LIFO: LIFO stands for "Last-In, First-Out." It refers to a data structure where the last element added to the structure is the first one to be removed. Think of it like a stack of plates where you add plates to the top and remove them from the top. The most recently added item is the one that gets removed next.

   In C, you can implement a LIFO data structure using arrays or linked lists. The main operations associated with a LIFO structure are "push" (to add an element) and "pop" (to remove the top element).

2. FIFO: FIFO stands for "First-In, First-Out." It refers to a data structure where the first element added to the structure is the first one to be removed. This is similar to a queue of people waiting in line, where the person who joined the line first is the one who gets served first.

   In C, you can implement a FIFO data structure using arrays or linked lists as well. The main operations associated with a FIFO structure are "enqueue" (to add an element) and "dequeue" (to remove the front element).

These concepts are fundamental in computer science and programming, and they are used in various applications to manage data in a specific order depending on the use case. Stacks and queues are often used as building blocks for more complex algorithms and data structures.
</details>

<details>
<summary><h3>What is a stack, and when to use it</h3></summary>

A stack is a linear data structure in computer science that follows the Last-In, First-Out (LIFO) principle. This means that the last element added to the stack is the first one to be removed. It's similar to stacking plates on top of each other, where you can only remove the top plate.

A stack has two primary operations:

1. **Push:** This operation adds an element to the top of the stack.

2. **Pop:** This operation removes the top element from the stack.

Additionally, there is often an operation called "peek" that allows you to view the top element without removing it.

Stacks are particularly useful in situations where you need to keep track of a collection of elements with a specific order and where you're interested in managing elements in a last-in, first-out manner. Here are some common scenarios where stacks are used:

1. **Function Call Stack:** In programming languages, a call stack is used to keep track of function calls. Each time a function is called, its context is pushed onto the stack. When the function completes, its context is popped from the stack, allowing the program to resume at the point where the function was called.

2. **Expression Evaluation:** Stacks are used in evaluating expressions, especially arithmetic expressions. Operators and operands are pushed onto the stack, and when an operator is encountered, the necessary operands are popped, the operation is performed, and the result is pushed back onto the stack.

3. **Undo/Redo Operations:** Stacks are commonly used in applications that support undo and redo functionalities. Each action is pushed onto the undo stack, and redo operations can be performed by popping from the undo stack and pushing onto a redo stack.

4. **Parsing and Syntax Checking:** Stacks are used in parsing and syntax checking of programming languages. They help keep track of open and closing parentheses, brackets, and braces, ensuring the code has balanced and correct syntax.

5. **Backtracking Algorithms:** Certain algorithms, like depth-first search in graph traversal, can utilize stacks to keep track of the exploration path and backtrack when needed.

6. **Reversing Data:** If you need to reverse the order of elements, a stack can be used to achieve this efficiently.

Overall, stacks are a versatile and powerful data structure with applications in various areas of computer science and programming whenever you need to manage data in a last-in, first-out manner.
</details>

<details>
<summary><h3>What is a queue, and when to use it</h3></summary>
</details>

<details>
<summary><h3>What are the common implementations of stacks and queues</h3></summary>
</details>

<details>
<summary><h3>What are the most common use cases of stacks and queues</h3></summary>
</details>

<details>
<summary><h3>What is the proper way to use global variables</h3></summary>
</details>

# Requirements
<details>
<summary><h3>General</h3></summary>

- Allowed editors: `vi`, `vim`, `emacs`
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A `README.md` file, at the root of the folder of the project is mandatory
- Your code should use the `Betty` style. It will be checked using [betty-style.pl](https://github.com/alx-tools/Betty/blob/master/betty-style.pl) and [betty-doc.pl](https://github.com/alx-tools/Betty/blob/master/betty-doc.pl)
- You are not allowed to use global variables
- No more than 5 functions per file
- You are allowed to use the C standard library
- The prototypes of all your functions should be included in your header file called `monty.h`
- All your header files should be include guarded
- You are expected to do the tasks in the order shown in the project
- Don’t forget to push your header file
</details>

<details>
<summary><h3>GitHub</h3></summary>

**There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.**
</details>

# More Info
<details>
<summary><h3>Data structures</h3></summary>

Please use the following data structures for this project. Don’t forget to include them in your header file.
```c
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
```c
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
</details>

<details>
<summary><h3>Compilation & Output</h3></summary>

- Your code will be compiled this way:
   ```bash
   $ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
   ```
- Any output must be printed on `stdout`
- Any error message must be printed on `stderr`
   - [Here is a link to a GitHub repository](https://github.com/ku1ik/stderred) that could help you making sure your errors are printed on `stderr`
</details>

<details>
<summary><h3>Tests</h3></summary>

We strongly encourage you to work all together on a set of tests
</details>

<details>
<summary><h3>The Monty language</h3></summary>

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

**Monty byte code files**

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:
```bash
julien@ubuntu:~/monty$ cat -e bytecodes/000.m
push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$
julien@ubuntu:~/monty$
```
Monty byte code files can contain blank lines (empty or made of spaces only, and any additional text after the opcode or its required argument is not taken into account:
```bash
julien@ubuntu:~/monty$ cat -e bytecodes/001.m
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
julien@ubuntu:~/monty$
```
<br>

**The monty program**

- Usage: `monty file`
    - where `file` is the path to the file containing Monty byte code
- If the user does not give any file or more than one argument to your program, print the error message `USAGE: monty file`, followed by a new line, and exit with the status `EXIT_FAILURE`
- If, for any reason, it’s not possible to open the file, print the error message `Error: Can't open file <file>`, followed by a new line, and exit with the status `EXIT_FAILURE`
    - where `<file>` is the name of the file
- If the file contains an invalid instruction, print the error message `L<line_number>: unknown instruction <opcode>`, followed by a new line, and exit with the status `EXIT_FAILURE`
    - where is the line number where the instruction appears.
    - Line numbers always start at 1
- The monty program runs the bytecodes line by line and stop if either:
    - it executed properly every line of the file
    - it finds an error in the file
    - an error occured
- If you can’t malloc anymore, print the error message `Error: malloc failed`, followed by a new line, and exit with status `EXIT_FAILURE`.
- You have to use `malloc` and `free` and are not allowed to use any other function from `man malloc` (realloc, calloc, …)
</details>

# Tasks
<details>
<summary>

### 0. push, pall
`mandatory`

</summary>

Implement the `push` and `pall` opcodes.

**The push opcode**

The opcode `push` pushes an element to the stack.

- Usage: `push <int>`
    - where `<int>` is an integer
- if `<int>` is not an integer or if there is no argument given to `push`, print the error message `L<line_number>: usage: push integer`, followed by a new line, and exit with the status `EXIT_FAILURE`
    - where is the line number in the file
- You won’t have to deal with overflows. Use the `atoi` function

**The pall opcode**

The opcode `pall` prints all the values on the stack, starting from the top of the stack.

- Usage `pall`
- Format: see example
- If the stack is empty, don’t print anything
```bash
julien@ubuntu:~/monty$ cat -e bytecodes/00.m
push 1$
push 2$
push 3$
pall$
julien@ubuntu:~/monty$ ./monty bytecodes/00.m
3
2
1
julien@ubuntu:~/monty$
```
</details>

<details>
<summary>

### 1. pint
`mandatory`

</summary>

Implement the `pint` opcode.

**The pint opcode**

The opcode `pint` prints the value at the top of the stack, followed by a new line.
- Usage: `pint`
- If the stack is empty, print the error message `L<line_number>: can't pint, stack empty`, followed by a new line, and exit with the status `EXIT_FAILURE`
```bash
julien@ubuntu:~/monty$ cat bytecodes/06.m 
push 1
pint
push 2
pint
push 3
pint
julien@ubuntu:~/monty$ ./monty bytecodes/06.m 
1
2
3
julien@ubuntu:~/monty$ 
```
</details>

<details>
<summary>

### 2. pop
`mandatory`

</summary>

Implement the `pop` opcode.

**The pop opcode**

The opcode `pop` removes the top element of the stack.
- Usage: `pop`
- If the stack is empty, print the error message `L<line_number>: can't pop an empty stack`, followed by a new line, and exit with the status `EXIT_FAILURE`
```bash
julien@ubuntu:~/monty$ cat bytecodes/07.m 
push 1
push 2
push 3
pall
pop
pall
pop
pall
pop
pall
julien@ubuntu:~/monty$ ./monty bytecodes/07.m 
3
2
1
2
1
1
julien@ubuntu:~/monty$ 
```
</details>

<details>
<summary>

### 3. swap
`mandatory`

</summary>

Implement the `swap` opcode.

**The swap opcode**

The opcode `swap` swaps the top two elements of the stack.
- Usage: `swap`
- If the stack contains less than two elements, print the error message `L<line_number>: can't swap, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
```bash
julien@ubuntu:~/monty$ cat bytecodes/09.m 
push 1
push 2
push 3
pall
swap
pall
julien@ubuntu:~/monty$ ./monty bytecodes/09.m 
3
2
1
2
3
1
julien@ubuntu:~/monty$ 
```
</details>

<details>
<summary>

### 4. add
`mandatory`

</summary>

Implement the `add` opcode.

**The add opcode**

The opcode add adds the top two elements of the stack.
- Usage: `add`
- If the stack contains less than two elements, print the error message `L<line_number>: can't add, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter
```bash
julien@ubuntu:~/monty$ cat bytecodes/12.m 
push 1
push 2
push 3
pall
add
pall

julien@ubuntu:~/monty$ ./monty bytecodes/12.m 
3
2
1
5
1
julien@ubuntu:~/monty$
```
</details>

<details>
<summary>

### 5. nop
`mandatory`

</summary>

Implement the `nop` opcode.

**The nop opcode**

The opcode `nop` doesn’t do anything.
- Usage: `nop`
</details>

<details>
<summary>

### 6. sub
`#advanced`

</summary>

Implement the `sub` opcode.

**The sub opcode**

The opcode `sub` subtracts the top element of the stack from the second top element of the stack.
- Usage: `sub`
- If the stack contains less than two elements, print the error message `L<line_number>: can't sub, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter
```bash
julien@ubuntu:~/monty$ cat bytecodes/19.m 
push 1
push 2
push 10
push 3
sub
pall
julien@ubuntu:~/monty$ ./monty bytecodes/19.m 
7
2
1
julien@ubuntu:~/monty$
```
</details>

<details>
<summary>

### 7. div
`#advanced`

</summary>

Implement the `div` opcode.

**The div opcode**

The opcode `div` divides the second top element of the stack by the top element of the stack.
- Usage: `div`
- If the stack contains less than two elements, print the error message `L<line_number>: can't div, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter
- If the top element of the stack is `0`, print the error message `L<line_number>: division by zero`, followed by a new line, and exit with the status `EXIT_FAILURE`
</details>

<details>
<summary>

### 8. mul
`#advanced`

</summary>

Implement the `mul` opcode.

**The mul opcode**

The opcode `mul` multiplies the second top element of the stack with the top element of the stack.
- Usage: `mul`
- If the stack contains less than two elements, print the error message `L<line_number>: can't mul, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter
</details>

<details>
<summary>

### 9. mod
`#advanced`

</summary>

Implement the `mod` opcode.

**The mod opcode**

The opcode `mod` computes the rest of the division of the second top element of the stack by the top element of the stack.
- Usage: `mod`
- If the stack contains less than two elements, print the error message `L<line_number>: can't mod, stack too short`, followed by a new line, and exit with the status `EXIT_FAILURE`
- The result is stored in the second top element of the stack, and the top element is removed, so that at the end:
    - The top element of the stack contains the result
    - The stack is one element shorter
- If the top element of the stack is `0`, print the error message `L<line_number>: division by zero`, followed by a new line, and exit with the status `EXIT_FAILURE`
</details>

<details>
<summary>

### 10. comments
`#advanced`

</summary>

Every good language comes with the capability of commenting. When the first non-space character of a line is `#`, treat this line as a comment (don’t do anything).
</details>

<details>
<summary>

### 11. pchar
`#advanced`

</summary>

Implement the `pchar` opcode.

**The pchar opcode**

The opcode `pchar` prints the char at the top of the stack, followed by a new line.
- Usage: `pchar`
- The integer stored at the top of the stack is treated as the ascii value of the character to be printed
- If the value is not in the ascii table (man ascii) print the error message `L<line_number>: can't pchar, value out of range`, followed by a new line, and exit with the status `EXIT_FAILURE`
- If the stack is empty, print the error message `L<line_number>: can't pchar, stack empty`, followed by a new line, and exit with the status `EXIT_FAILURE`
```bash
julien@ubuntu:~/monty$ cat bytecodes/28.m 
push 72
pchar
julien@ubuntu:~/monty$ ./monty bytecodes/28.m 
H
julien@ubuntu:~/monty$
```
</details>

<details>
<summary>

### 12. pstr
`#advanced`

</summary>

Implement the `pstr` opcode.

**The pstr opcode**

The opcode `pstr` prints the string starting at the top of the stack, followed by a new line.
- Usage: `pstr`
- The integer stored in each element of the stack is treated as the ascii value of the character to be printed
- The string stops when either:
    - the stack is over
    - the value of the element is 0
    - the value of the element is not in the ascii table
- If the stack is empty, print only a new line
```bash
julien@ubuntu:~/monty$ cat bytecodes/31.m 
push 1
push 2
push 3
push 4
push 0
push 110
push 0
push 108
push 111
push 111
push 104
push 99
push 83
pstr
julien@ubuntu:~/monty$ ./monty bytecodes/31.m 
School
julien@ubuntu:~/monty$
```
</details>

<details>
<summary>

### 13. rotlrt
`#advanced`

</summary>

Implement the `rotl` opcode.

**The rotl opcode**

The opcode `rotl` rotates the stack to the top.
- Usage: rotl
- The top element of the stack becomes the last one, and the second top element of the stack becomes the first one
- `rotl` never fails
```bash
julien@ubuntu:~/monty$ cat bytecodes/35.m 
push 1
push 2
push 3
push 4
push 5
push 6
push 7
push 8
push 9
push 0
pall
rotl
pall
julien@ubuntu:~/monty$ ./monty bytecodes/35.m 
0
9
8
7
6
5
4
3
2
1
9
8
7
6
5
4
3
2
1
0
julien@ubuntu:~/monty$ 
```
</details>

<details>
<summary>

### 14. rotr
`#advanced`

</summary>

Implement the `rotr` opcode.

**The rotr opcode**

The opcode `rotr` rotates the stack to the bottom.
- Usage: `rotr`
- The last element of the stack becomes the top element of the stack
- `rotr` never fails
</details>

<details>
<summary>

### 15. stack, queue
`#advanced`

</summary>

Implement the `stack` and `queue` opcodes.

**The stack opcode**

The opcode `stack` sets the format of the data to a stack (LIFO). This is the default behavior of the program.

- Usage: `stack`

**The queue opcode**

The opcode `queue` sets the format of the data to a queue (FIFO).

- Usage: `queue`

When switching mode:

- The top of the stack becomes the front of the queue
- The front of the queue becomes the top of the stack
```bash
julien@ubuntu:~/monty$ cat bytecodes/47.m
queue
push 1
push 2
push 3
pall
stack
push 4
push 5
push 6
pall
add
pall
queue
push 11111
add
pall
julien@ubuntu:~/monty$ ./monty bytecodes/47.m
1
2
3
6
5
4
1
2
3
11
4
1
2
3
15
1
2
3
11111
julien@ubuntu:~/monty$ 
```
</details>

<details>
<summary>

### 16. Brainf*ck
`#advanced`

Directory: [bf]()

File: [1000-school.bf]()
</summary>

Write a Brainf*ck script that prints `School`, followed by a new line.
- All your Brainf*ck files should be stored inside the `bf` sub directory
- You can install the bf interpreter to test your code: `sudo apt-get install bf`
- Read: [Brainf*ck](https://en.wikipedia.org/wiki/Brainfuck)
```bash
julien@ubuntu:~/monty/bf$ bf 1000-school.bf 
School
julien@ubuntu:~/monty/bf$ 
```
</details>

<details>
<summary>

### 17. Add two digits
`#advanced`

Directory: [bf]()

File: [1001-add.bf]()
</summary>

Add two digits given by the user.
- Read the two digits from stdin, add them, and print the result
- The total of the two digits with be one digit-long (<10)
```bash
julien@ubuntu:~/monty/bf$ bf ./1001-add.bf
81
9julien@ubuntu:~/monty/bf$
```
</details>

<details>
<summary>

### 18. Multiplication
`#advanced`

Directory: [bf]()

File: [1002-mul.bf]()
</summary>

Multiply two digits given by the user.
- Read the two digits from stdin, multiply them, and print the result
- The result of the multiplication will be one digit-long (<10)
```bash
julien@ubuntu:~/monty/bf$ bf 1002-mul.bf
24
8julien@ubuntu:~/monty/bf$
```
</details>

<details>
<summary>

### 19. Multiplication level up
`#advanced`

Directory: [bf]()

File: [1003-mul.bf]()
</summary>

Multiply two digits given by the user.
- Read the two digits from stdin, multiply them, and print the result, followed by a new line
```bash
julien@ubuntu:~/monty/bf$ bf 1003-mul.bf 
77
49
julien@ubuntu:~/monty/bf$ 
```
</details>

