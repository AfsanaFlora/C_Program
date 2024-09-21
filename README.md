1. What did you need to do to install the language?

Since we're using VS Code, here’s the step-by-step installation process for C++:
•	Install the C++ Compiler:
o	For Windows: Download and install MinGW from its official website. During installation, select the packages for mingw32-gcc-g++ (C++ compiler). After installation, add the MinGW bin folder to the system's PATH environment variable.
•	Set Up Visual Studio Code:
  1.	Download and install VS Code from the official website if you haven't already.
  2.	Install the C/C++ extension by Microsoft:
	Open VS Code, click on the Extensions icon on the sidebar (or press Ctrl+Shift+X).
	Search for "C/C++" and install the extension provided by Microsoft.
2. Does this language come with a recommended programming environment?
C++ does not have a specific recommended IDE, but Visual Studio Code is an excellent choice due to its flexibility and lightweight nature. You’ll use the C/C++ extension for IntelliSense and debugging.
3. How do you run programs in that language?
In VS Code, after writing the program, you can follow these steps:
1.	Write the C++ code:
o	Create a new file, and name it hello_world.cpp.
o	Write your C++ code inside this file.
2.	Set up the build task (to compile C++ programs):
o	Press Ctrl+Shift+B and choose C++: g++.exe build active file.
o	VS Code will automatically create a tasks.json file, where you can configure how the program is built.
3.	Compile and run the program:
o	To compile the program, you can press Ctrl+Shift+B. This will use the build task created earlier.
o	To run the compiled program, open the terminal in VS Code (`Ctrl+``) and type the following to execute the program:  ./hello_world
Alternatively, if you installed the Code Runner extension:
•	After writing the code, simply press Ctrl+Alt+N to run the program directly from within VS Code.
4. How do you write comments in your language?
In C++, you can write comments in two ways:
•	Single-line comments: Use // at the beginning of the line.
// This is a single-line comment
•	Multi-line comments: Enclose the comment block between /* and */.
/* This is a 
   multi-line comment */



