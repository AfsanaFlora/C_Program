# C++ Project Title

A brief description of your C++ project, its features, and its purpose.

## Table of Contents
- [Language History, Overview and Setup](#language-overview-and-setup)
- [Data Types and Syntax Conventions](#data-types-and-syntax-conventions)
- [Control Flow](#control-flow)
- [Functions and Parameters](#functions-and-parameters)
- [Naming, Scope, and Bindings](#naming-scope-and-bindings)
- [Plan for Final Project Programming Task](#plan-for-final-project-programming-task)
- [Check-in for Final Project](#check-in-for-final-project)
- [Final Programming Project and Presentations](#final-programming-project-and-presentations)
- [Installation](#installation)
- [Usage](#usage)


## Language History, Overview and Setup

C++ is a powerful general-purpose programming language widely used for system/software development and game development. 


### History

**Bjarne Stroustrup** founded C++ in Bell Laboratories in Murray Hill, New Jersey, in **1979**. It was created as an addition to the C programming language to strengthen **object-oriented programming** support and increase the effectiveness and adaptability of system and application development.


### application

C++ is primarily used for:
  * **System programming** (operating systems, device drivers)
  * **Application programming** (software applications, GUIs)
  * **Game development** (high-performance games)
  * **Embedded systems** (automobiles, appliances)
  * **Real-time systems** (financial systems, telecommunications)

### Sources for Learning and Reference Materials

When starting to program in C++, I will refer to various resources, including:
**Books:**
 - "C++ Primer" by Stanley B. Lippman, Josée Lajoie, and Barbara E. Moo
 - "Effective C++" by Scott Meyers
**Websites:**
 - [cplusplus.com](http://www.cplusplus.com) - A comprehensive resource for C++ tutorials and references
 - [cppreference.com](https://en.cppreference.com) - A detailed reference for C++ standard libraries
**Online courses:**
 - Platforms like **Coursera** and **Udemy** offer C++ programming courses.
 - **Forums and Communities:**
 Stack Overflow and the C++ subreddit are good places to ask questions and find solutions.


## Since we're using VS Code, here’s the step-by-step installation process for C++:

 ### Installation 
1. **Install Visual Studio**:
   - Download from [Visual Studio](https://visualstudio.microsoft.com/).
   - Install the C/C++ extension by Microsoft:
   *	Open VS Code, click on the Extensions icon on the sidebar (or press `Ctrl+Shift+X`).
   *	Search for "C/C++" and install the extension provided by Microsoft.

2. **Install the C++ Compiler**:

Common preinstalled compilers on various systems are the **Clang** tools with **Xbox** on macOS and the **GNU Compiler Collection (GCC)** on Linux.

TO check if you already have it in your PC:
 1. Open a new VS Code terminal window using (Ctrl+Shift+`)

2. Use the following command to check for the GCC compiler `g++`:

```cpp

g++ --version
```
Or use this command for Clang compiler `clang`: 

```cpp

clang --version
```
The output should display the compiler version and its details. If you don't see this information, ensure that your compiler executable is included in your platform path (`%PATH` on Windows, `$PATH` on Linux and macOS) so that the C/C++ extension can locate it. If it's not available, follow the instructions in the section below to install a compiler.

 ## For Windows: 
  Watch the [MinGW tutorial](https://code.visualstudio.com/docs/cpp/config-mingw#_prerequisites).

  ## For Linux:
  Watch the [GCC tutorial](https://code.visualstudio.com/docs/cpp/config-linux#_prerequisites).

  ## macOS:
  Watch the [GCC tutorial](https://code.visualstudio.com/docs/cpp/config-clang-mac#_prerequisites).


## Getting Started

C++ does not have a specific recommended IDE, but Visual Studio Code is an excellent choice due to its flexibility and lightweight nature. You’ll use the C/C++ extension for IntelliSense and debugging.

In VS Code, after writing the program, you can follow these steps:

  1.	Write the C++ code:
	 * Create a new file, and name it `hello_world.cpp`.
     * Write your C++ code inside this file.

  2.	Set up the build task (to compile C++ programs):
     * Press **Ctrl+Shift+B** and choose `C++: g++.exe` build active file.
     * VS Code will automatically create a `tasks.json` file, where you can configure how the program is built.
  3.	Compile and run the program:
     *	To compile the program, you can press **Ctrl+Shift+B**. This will use the build task created earlier.
     * To run the compiled program, open the terminal in VS Code (**Ctrl+**) and type the following to execute the program:  `./hello_world`

Alternatively, if you installed the Code Runner extension:
 After writing the code, simply press **Ctrl+Alt+N** to run the program directly from within VS Code.


### "Hello, World"
Here's a simple C++ program to print "Hello, World!":

```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
} 
```
## Writing Comments

In C++, you can write comments in two ways:
* **Single-line comments**: Use // at the beginning of the line.

```cpp
// This is a single-line comment
```

* **Multi-line comments**: Enclose the comment block between /* and */.

```cpp
/* This is a 
   multi-line comment */
```

## Data Types and Syntax Conventions

- `int`: Integer data type.
- `float`: Floating-point data type.
- `double`: Double-precision floating-point.
- `char`: Character type.

### Syntax Example
```cpp
int number = 10;
float pi = 3.14f;
char letter = 'A';
```

## Control Flow
Control flow statements allow you to dictate the order of execution in your program. Common statements include:

* If statements
* Switch statements
* Loops (``` for, while, and do-while ```)

### Example of Control Flow
```cpp
if (number > 0) {
    std::cout << "Positive number" << std::endl;
} else {
    std::cout << "Non-positive number" << std::endl;
}
```

## Functions and Parameter
Functions in C++ are code blocks that carry out a specific goal. A function can operate with different types of data by accepting parameters as input values.

### Function Syntax:

```cpp
return_type function_name(parameter1, parameter2, ...) {
    // function body
    // code to be executed
    return value; // If the function returns a value
}
```
### Example

```cpp
#include <iostream>

// Function to add two numbers
int add(int x, int y) {
    return x + y;
}

int main() {
    int a = 5;
    int b = 10;

    // Calling the add function with parameters
    int sum = add(a, b);

    std::cout << "The sum is: " << sum << std::endl;

    return 0;
}
```


