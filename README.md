# **0x19. C - STACKS, QUEUES - LIFO, FIFO**
`C` `Group project` `Algorithm` `Data structure`

# Resources
- [Google]()
- [How do I use extern to share variables between source files in C?](https://stackoverflow.com/questions/1433204/how-do-i-use-extern-to-share-variables-between-source-files)
- [Stacks and Queues in C](https://data-flair.training/blogs/stacks-and-queues-in-c/)
- [Stack operations](https://www.digitalocean.com/community/tutorials/stack-in-c)
- [Queue operations](https://www.edureka.co/blog/queue-in-c/)

<!-- man or help:
- `` -->

# Learning Objectives
<details>
<summary><h3>What do LIFO and FIFO mean</h3></summary>
</details>

<details>
<summary><h3>What is a stack, and when to use it</h3></summary>
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
<summary><h3></h3></summary>


</details>

# Tasks
<details>
<summary>

### 0. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 1. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 2. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 3. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 4. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 5. 
`mandatory`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

<details>
<summary>

### 
`#advanced`

File: []()
</summary>


</details>

