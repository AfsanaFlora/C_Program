# C++ Project Title

A brief description of your C++ project, its features, and its purpose.

## Table of Contents
- [Language History, Overview and Setup](#language-history-overview-and-setup)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [Writing Comments](#writing-comments)
- [Naming Conventions in C++](#naming-conventions-in-c)
- [Data Types and Syntax Conventions](#data-types-and-syntax-conventions)
- [Control Flow](#control-flow)
- [Functions and Parameters](#functions-and-parameters-and-parameters)
- [Pass-by-Reference vs Pass-by-Value in C++](#pass-by-reference-vs-pass-by-value-in-c)
- [Limitations of C++](#limitations-of-c)


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
The output should display the compiler version and its details. If you don't see this information, ensure that your compiler executable is included in your platform path (`%PATH` on Windows, `$PATH` on Linux and macOS) so that the C/C++ extension can locate it. 

If it's not available, follow the instructions in the section below to install a compiler.

 ### For Windows: 
  Watch the [MinGW tutorial](https://code.visualstudio.com/docs/cpp/config-mingw#_prerequisites).

 ### For Linux:
  Watch the [GCC tutorial](https://code.visualstudio.com/docs/cpp/config-linux#_prerequisites).

 ### macOS:
  Watch the [GCC tutorial](https://code.visualstudio.com/docs/cpp/config-clang-mac#_prerequisites).


## Getting Started

C++ does not have a specific recommended IDE, but Visual Studio Code is an excellent choice due to its flexibility and lightweight nature. You’ll use the C/C++ extension for IntelliSense and debugging.

In VS Code, after writing the program, you can follow these steps:

1. Write the C++ code:
 * Create a new file, and name it `hello_world.cpp`.
 * Write your C++ code inside this file.

2. Set up the build task (to compile C++ programs):
 * Press **Ctrl+Shift+B** and choose `C++: g++.exe` build active file.
 * VS Code will automatically create a `tasks.json` file, where you can configure how the program is built.

3. Compile and run the program:
 * To compile the program, you can press **Ctrl+Shift+B**. This will use the build task created earlier.
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

## Naming Conventions in C++

**Case Sensitivity**: C++ is case-sensitive, so `myVariable` and `MyVariable` are different.

**Starting Character**: Variable names must start with a letter or an underscore. They cannot start with a digit or special symbols like `@`, `#`, `$`.

**Camel Case vs. Snake Case**: It’s common to see both camelCase (`lastName`) and snake_case (`last_name`) in C++, but camelCase is often preferred in many C++ coding standards.


## Data Types and Syntax Conventions

- `int`: Integer data type.
- `float`: Floating-point data type.
- `double`: Double-precision floating-point.
- `char`: Character type.
- `std::string`: Stores a sequence of characters (text).
- `bool`: Stores true or false values.
- `std::vector`: Stores a list of elements of the same type.
- `std::map`: Stores key-value pairs, similar to a dictionary in other languages

### Syntax Example
```cpp
#include <iostream>
#include <string>
#include <vector>
#include <map>

int main() {
    // Integer
    int age = 21;
    std::cout << "Age: " << age << std::endl;

    // String
    std::string name = "Afsana";
    std::cout << "Name: " << name << std::endl;

    // Floating-point number
    float height = 5.5f;
    std::cout << "Height: " << height << " feet" << std::endl;

    // Boolean
    bool isStudent = true;
    std::cout << "Is student: " << std::boolalpha << isStudent << std::endl;

    // Array (using a vector in C++)
    std::vector<int> scores = {85, 90, 95};
    std::cout << "First score: " << scores[0] << std::endl;

    // Dictionary (std::map in C++)
    std::map<std::string, int> studentGrades;
    studentGrades["Math"] = 90;
    studentGrades["Science"] = 88;
    std::cout << "Math grade: " << studentGrades["Math"] << std::endl;

    // Mixed-type operation (int + float)
    int a = 10;
    float b = 3.5;
    float result = a + b; // Widening conversion, int is promoted to float
    std::cout << "Result of int + float: " << result << std::endl;

    // Explicit type casting
    std::string strNum = "100";
    int num = std::stoi(strNum); // Converting string to int
    std::cout << "String to int: " << num << std::endl;

    // Division example
    int num1 = 7;
    int num2 = 2;
    float divisionResult = num1 / (float)num2; // Explicit casting
    std::cout << "Division result: " << divisionResult << std::endl;

    return 0;
}

```

### Explanation of Code

**Basic Data Types**:
 The code shows examples of declaring variables with common data types in C++—int, float, bool, string, vector (array), and map (dictionary).

**Mixed Type Operations**:
 C++ allows you to mix types like int and float. In such cases, C++ will usually promote the narrower type (int) to the wider type (float), leading to a widening conversion.

**Type Conversion**:
 C++ supports both implicit (automatic) and explicit (manual) type conversions. For example, dividing two integers will result in an integer unless you explicitly cast one of them to float for floating-point division.

## Important Notes:
Before you begin learning or working with a programming language, there are some key points you need to understand:

* **Keywords or Reserved Words**: C++ has 97 reserved keywords (e.g., `int`, `float`, `if`, `while`, `return`), which cannot be used as variable names.

* **Variable Naming Requirements**: In C++, variable names must begin with a letter or an underscore. They cannot start with a number or special characters. Although `camelCase` or `snake_case` is a style choice, it's not enforced by the compiler, only by community standards.

* **Statically Typed**: C++ is a *statically-typed* language, meaning variable types are determined at compile time.

* **Strongly Typed**: C++ is *strongly typed*, meaning it requires explicit type conversion when types do not match.

* **Mutability**: Most variables in C++ are *mutable* by default, but you can make them *immutable* using the const keyword.

* **Operators**: Operators such as `+`, `-`, `*` and `/` work with numeric types, while `==`, `!=`, `&&` and `||` apply to boolean logic.

* **Mixed Type Operations**: C++ supports mixed-type operations. The result usually depends on the types involved; for example, adding `int` and `float` results in a `float`.

* **Binding of Variables and Operators**: Variable names and their types are bound during compilation in C++, and operators like `+` or `*` are also bound to the types they operate on at compile time.

* **Explicitly typed**: C++ is explicitly typed, meaning you must explicitly declare the type of each variable when you create it.

## Example of a Type Error
If you write this in C++:

```cpp
std::string x = "5" + 6; // This will not compile
``` 

It will result in a compilation error because C++ does not implicitly convert between string and int. You need to explicitly convert int to string:

```cpp
std::string x = "5" + std::to_string(6); // Correct way
```

## Limitations of C++

* **Adding Ints and Floats**: Adding `int` and `float` is allowed, and the result will be a `float`.

* **Arrays**: In C++, an array (or vector) cannot store mixed data types by default.

* **Implicit vs Explicit Conversions**: Conversions like `int` to `float` are implicit, but `string` to `int` requires an explicit conversion.


### Complex Data Types
C++ has complex data types such as `std::vector`, `std::map` and `std::pair`, which are commonly used for storing collections and mapping relationships.


## Control Flow
Control flow statements allow you to dictate the order of execution in your program. Common statements include:

* If statements
* Switch statements
* Loops (``` for, while, and do-while ```)


### Example of Control Flow

**Example of `if` statement**:

```cpp
if (number > 0) {
    std::cout << "Positive number" << std::endl;
} else {
    std::cout << "Non-positive number" << std::endl;
}
```


**Example of `switch` statement**:
```cpp
int main() {
    int day = 2;

    switch (day) {
        case 1:
            cout << "Monday";
            break;
        case 2:
            cout << "Tuesday";
            break;
        case 3:
            cout << "Wednesday";
            break;
        default:
            cout << "Invalid day";
    }

    return 0;
}
```

**Example of `Loop`**:

```cpp
int main() {
    // Loop to print numbers from 1 to 5
    for (int i = 1; i <= 5; i++) {
        cout << "Number: " << i << endl;
    }

    return 0;
}
```

## Functions and Parameters
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

 ### Function Declaration Syntax in C++
In C++, the syntax for declaring a function is straightforward:

```cpp
return_type function_name(parameter_list) {
    // function body
}
```
### Notes:
 * **Return Type**: The type of value that the function will take e.g. `int`, `double`, `void` etc.

 * **Function Name**: The name you give to a function which is used to call that function in a program.
 
 * **Parameter List**: A set of separate input(s) to the function (if any), which may have any data type.
 
 * **Function Body**: The code that the function will execute If you know that there will be a basic structure to most of the forms you create, several keystrokes can be saved with a simple menu macro.
  *Example*: Multiplying Two Numbers

***Multiplying Two Numbers***
```cpp
int multiply(int a, int b) {
    return a * b;
}
```

This function accepts two integer parameters (a and b) and computes the product of the said parameters. This is a flexibility you have while using this kind of function; you can call this function any number of times using different values.

## Recursive Function
C++ can use Recursion - it is the ability of a function to call that same function in its code. Recursion is often used for problems such as finding the factorial of a number for example.



***Example: Recursive Factorial Function***

```cpp
int factorial(int n) {
    if (n == 0) {
        return 1;  // Base case
    }
    return n * factorial(n - 1);  // Recursive case
}
```

This function calculates the factorial of n by calling itself with `n - 1` until it reaches the base case where `n == 0`.

## Function Returning Multiple Values

Functions That Returns More Than One Value

That is, any C++ function can only return a value in one data type but there are ways for getting around this. One of the common solutions is to return a `std::pair` or `std::tuple`. This manifests a way of packaging multiple return values.

***Example: Splitting a String into Two Parts***
```cpp
#include <iostream>
#include <string>
#include <utility>  // For std::pair

std::pair<std::string, std::string> splitString(const std::string& str) {
    size_t mid = str.length() / 2;
    return {str.substr(0, mid), str.substr(mid)};
}

int main() {
    std::string text = "HelloWorld";
    auto result = splitString(text);
    std::cout << "First part: " << result.first << "\n";
    std::cout << "Second part: " << result.second << "\n";
    return 0;
}
```

This function splits the string `HelloWorld` into two parts (`Hello` and `World`) and returns them using `std::pair`.


## Pass-by-Reference vs Pass-by-Value in C++
In fact, passing parameters to a function in C++ it has two types: **pass by value** and **pass by reference**. In fact, every argument is **passed by value**; this implies that in order to transmit an argument into a function, a copy of the variable will be made. The ability to create local variables means that improvements inside the function do not inflict upon the outside variable.

But if you wish to alter the actual variable that was passed, you can use a reference by assigning & before the variable.

***Example: Pass-by-Value vs Pass-by-Reference***

```cpp
#include <iostream>

// Pass-by-value
void passByValue(int a) {
    a = 100;
}

// Pass-by-reference
void passByReference(int& a) {
    a = 100;
}

int main() {
    int num = 50;

    passByValue(num);
    std::cout << "After passByValue: " << num << "\n";  // Still 50

    passByReference(num);
    std::cout << "After passByReference: " << num << "\n";  // Now 100

    return 0;
}
```
In the first case (`passByValue`), the value of num remains unchanged because a copy is passed. In the second case (`passByReference`), the original `num` is modified.


### Notes:

**Function Declaration Rules**

In C++, functions can be declared anywhere in the file, that is, before or after the main function. However, if you define a function *after* it's called, you must provide a *function prototype* before the call.

**Recursive Functions**
C++ supports recursive functions, as shown in the factorial example. The key is having a base case to prevent infinite recursion.

**Multiple Parameters**
Functions in C++ can accept multiple parameters of different types:

```cpp
void printDetails(int age, std::string name) {
    std::cout << "Name: " << name << ", Age: " << age << "\n";
}
```

**Returning Multiple Values**
C++ does not support returning multiple values directly.

**Pass by value versus Pass by Reference**
C++ supports both, pass and call by reference, although call by reference is the default option. While pass by value copies the argument of the function, pass by reference lets the function manipulate it directly.

**Argument Storage**
*Arguments*, *parameters*, and *local variables* are typically stored on the `stack`, which is faster and automatically managed in terms of scope and lifetime. If you allocate memory dynamically (e.g., with **new**), it is stored on the `heap`, and you must manage the memory manually.

**Scoping Rules**
 * **Global Variables**: Global in default, can be overridden at local scope in the course of the program.
 * **Local Variables**: Available only within the block where they are defined.
 * **Function Scope**: Any variable declared within a particular function, becomes the function’s local variable.
 * **Lifetime**: Local variables are defined as those variables that exist only while the particular function or block of code is executing. Global variables are valid only for the period that the program is running.

**Side Effects**
Side effects (when a `function` changes some element in the surrounding environment, for instance, using global variables or passing arguments by reference) are possible. Declared with `const`, it has advantages that protect some variables and objects from being modified in other parts of a program.

**Local Variable Storage**
Local variables are stored on `stack`, it is the memory area for calling of functions and the local variables. *new* creates objects in the heap space of the memory.

## Other Features of C++ Functions

**Overloading**: C++ supports function overloading, where multiple functions can have the same name but different parameter lists.

**Default Parameters**: You can specify default values for function parameters, allowing you to call a *function* with fewer *arguments*.

