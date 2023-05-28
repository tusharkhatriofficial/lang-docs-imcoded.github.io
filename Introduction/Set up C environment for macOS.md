# Set up C environment for macOS

To develop C programs on macOS, there are two things that we need:

1.  First, we need a **code editor** - this is the program that we will use to write our source code (a source code file is simply a text file, which has a ".c" extension, and which contains valid C code).
2.  Secondly, we need a **C compiler** - this is a program that converts the source code we have written into an executable file that we can run.



## Installing the command line tools

- Open Terminal: Open the Terminal app on your Mac. You can do this by searching for Terminal in Spotlight or by navigating to Applications > Utilities > Terminal.

- Install Xcode Command Line Tools: Type the following command in the Terminal window:

```zsh
xcode-select --install
```

  Press enter and follow the prompts to install the Xcode command line tools. This will install the necessary tools and libraries for C development on your Mac.
  
- Install a C Compiler: The C compiler is required for compiling and executing C programs. The most popular C compiler for macOS is the GCC compiler. To install GCC, you can use a package manager such as Homebrew. If you don't have Homebrew installed, run the following command in the Terminal window:

```zsh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

  This command will install Homebrew on your Mac. Next, install GCC by running the following command:

```zsh
brew install gcc
```

  This will download and install the GCC compiler on your Mac.

- Verify the Installation: To verify that the C compiler is installed correctly, run the following command:

```zsh
gcc --version
```

  This command will display the version of the GCC compiler installed on your Mac.
  
- Create a C Program: Now that you have installed the C compiler, you can create a simple C program to test the environment. Open a text editor and create a new file named "hello.c". Type the following code into the file:

```zsh
#include <stdio.h>

int main() {
    printf("Hello, World!");
    return 0;
}
```

  Save the file to your desktop.

- Compile and Run the Program: Open the Terminal and navigate to the directory where you saved the "hello.c" file. To compile the program, run the following command:

```zsh
gcc -o hello hello.c
```

  This command will compile the "hello.c" file and create an executable file named "hello". To run the program, type the following command:
  
```zsh
./hello
```

  This command will execute the "hello" program and display the output "Hello, World!" in the Terminal window.

That's it! You have successfully set up a C development environment on macOS and compiled and executed a C program.




## Installing code editor (Visual Studio Code)

- __Download and Install Visual Studio Code__: Download and install the latest version of VS Code for macOS from the official website at [https://code.visualstudio.com/download](https://code.visualstudio.com/download)

- __Install the C/C++ Extension__: Open VS Code and navigate to the Extensions view by clicking on the Extensions icon on the left-hand side of the screen or by using the shortcut key `⇧⌘X` (shift + command + X). In the search bar, search for "C/C++" and click on the "Install" button to install the extension.

- __Create a New C File__: Create a new file in VS Code by selecting "File" > "New File" or using the shortcut key `⌘N` (command + N). Save the file with a `.c` extension, for example "hello.c".

- __Write a Simple C Program__: In the new file, type the following code to create a simple "Hello, World!" program:

```c
#include <stdio.h>

int main() {
    printf("Hello, World!");
    return 0;
}
```

  Save the file.

- __Configure the C Compiler__: Open the Terminal and navigate to the directory where the C file is saved. To compile the program with GCC, run the following command:

```zsh
gcc -o hello hello.c
```

  This will create an executable file named "hello".

- __Configure the VS Code Launch Configuration__: In VS Code, open the "Run" view by clicking on the "Run" icon on the left-hand side of the screen or by using the shortcut key `⇧⌘D` (shift + command + D). Click on the "create a launch.json file" link and select "C++ (GDB/LLDB)" from the dropdown list.

- Configure the Launch Configuration Properties: In the launch.json file, add the following configuration properties:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "gcc - Build and debug active file",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}/${fileBasenameNoExtension}",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${fileDirname}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "lldb",
            "preLaunchTask": "gcc build active file",
        }
    ]
}
```

  Save the file.

- __Configure the Build Task__: In VS Code, open the "Tasks" view by clicking on the "Tasks" icon on the left-hand side of the screen or by using the shortcut key `⇧⌘B` (shift + command + B). Click on the "Configure Task" button and select "Create tasks.json file from template" and then select "Others".

- Configure the Build Task Properties: In the tasks.json file, add the following configuration properties:

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "type": "shell",
            "label": "gcc build active file",
            "command": "/usr/bin/gcc",
            "args": [
                "-g",
                "${file}",
                "-o",
                "${fileDirname}/${fileBasenameNoExtension}"
            ],
            "options": {
                "cwd": "${fileDirname}"
            },
            "problemMatcher": [
                "$gcc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
```

  Save the file.

> This task configuration uses the `gcc` command to compile the C file specified by `${file}` into an executable file named `${fileBasenameNoExtension}` in the same directory as the C file. The `-g` option adds debugging information to the executable file, which is useful for debugging your code later. The `problemMatcher` property specifies the regular expression used to match error messages produced by the compiler, and the `group` property specifies that this is the default build task for your project.

- Build the Program: Press the `⇧⌘B` (shift + command + B) key combination to build the program using the `gcc` build task you just configured. Alternatively, you can use the "Terminal" and run the command `Tasks: Run Build Task` from the VS Code Command Palette

- Run the Program: Once the build task has finished successfully, you can run the program by opening the "Terminal" and navigating to the directory where the executable file was created (i.e., `${fileDirname}`). Then, run the following command to execute the program:

```zsh
./<executable file name>
```

  For example, if your executable file is named `hello`, you would run the following command:

```zsh
./hello
```

  This should display the output of your C program in the terminal.

You have now successfully set up VS Code with the C compiler on your macOS and can build and run C programs using the editor.

