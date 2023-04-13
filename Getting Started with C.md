
## Set up a C development environment for Windows

Setting up a C development environment on Windows requires several steps. Below given is a basic guide to get you started:

### Installing C/GCC Compiler for Windows

Following are the steps to download and install the MinGW GCC Compiler for windows.

**Step 1**: Search MinGW C Compiler on the Web

  To download the MinGW compiler, go to your favorite browser and search MinGW C Compiler or click on the [sourceforge.net](https://www.google.com/search?q=mingw+c+compiler&rlz=1C1GCEA_enIN964IN964&oq=mingw+c+compiler&aqs=chrome..69i57j0i512l8.4872j0j15&sourceid=chrome&ie=UTF-8) link.

**Step 2**: Download MinGW.

  After clicking on the green-colored download button on the website, the MinGW setup file will start downloading.

**Step 3**: Locate the MinGW-get-setup.exe File and Start Installation.

  Locate the setup.exe file on your Downloads folder and double-click on it. After double-clicking on the setup file, MinGW Installation Manager Setup Tool will now open. It will show the information like version, name, etc. Click on the Install button and proceed to start the installation.
  
**Step 4**: Specify Installation Preferences.

  Now the installation manager will ask you to specify the installation preferences. For that, you will be asked to choose the installation directory. If you wish to change it, you can browse the explorer and specify the location as per your requirement. After that, click on continue to proceed further.

> It is recommended to install it in the default location.

**Step 5**: Download and Set up MinGW Installation Manager.

The installer will now automatically download the required files for MinGW to install on your Windows system. Grab a cup of coffee and wait patiently till the installation manager finishes downloading all the files. When it is done, click on continue to proceed ahead.

> Active internet is required throughout the installation process.

**Step 6**: Select Packages Required for the Compiler.

There are three packages required for the basic MinGW setup that you have to choose from the MinGW Installation Manager.

**MinGW32-base Package.**

First, you have to install the _MinGW32-base package_. This package is used to compile the C program, including linker and other binary tools. Right-click on the `MinGW32-base option` and select `Mark for Installation`.

**MinGW32-gcc-g++ Package.**

Now you have to install the `MinGW32-gcc-g++` package. This package is used to compile C++ source code. This is an optional component of the MinGW Compiler. It is only required if you are going to program in C++ language only. To select the `MinGW32-gcc-g++` right-click on it and select `Mark for Installation`.

**MinGW32-gcc-objc package.**

At last, you have to install the `MinGW32-gcc-objc` package. This package is used to compile objective C language. It is an optional component. It is only required if you are going to program in objective C. To select the `MinGW32-gcc-objc` package, right-click on it and select _Mark for Installation._

**Step 7**: Apply the Changes

After selecting all the required packages, go to I`nstallation>>Apply` Changes and click on `Apply Changes`.

**Step 8**: Download the Changes.

Now it is time to download all the packages you selected in the previous step. Click on `Apply` and proceed further to download and install them. The download for the packages will now begin, wait for a few minutes until the download completes.

**Step 9**: Installation Completed.

Now the installation has been completed, click on Close to close the Installation manager. To check if it is installed or not, open Command Prompt and type `g++ --version`.


> Error: Currently, the command prompt cannot detect the MinGW compiler (GCC) because the environment path variable has not been set. The environment path variable helps to detect the compiler in your whole system. It makes the alias name for the compiler, which denotes the path. Follow the steps below to set the environment path variable for MinGW on the Windows system.

##### Setting up Path Variable

To set up the path for the C compiler for windows, follows the below steps :

**Step 1**: Copy the path of the MinGW bin.

When you install the MinGW, it creates a folder named MinGW in C: Drive. To set the compiler's path, we need the path to the bin directory of MinGW.

-   Go to C:>MinGW>bin.
-   Now, inside the bin folder, click on the address bar and copy the address.
-   We require this address to be set as the path in the environment variable.
-   If your install location was somewhere else, you may go to that location where you have installed MinGW.

> If you open command prompt directly in the bin path, the `g++ --version` command will work properly, but the command should work on all the directories in the computer. That is the main reason to set the environment path variable.

**Step 2**: Open Edit System Variables.

Navigate to the search bar and type `Edit the system environment variables` and click on open to continue to edit system environment variables.

**Step 3**: Edit the Path.

In the `User` variables for the _User_ section, select the **path** and click on the `Edit` button.

**Step 4**: Setup a New Path.

-   After clicking on the `Edit button`, a new window, `Edit environment variable` will open. This window allows us to add the path as per our requirements.

- Since we want to add a new path, click on the New button. A new window, Edit environment variable, will open. This window allows us to add the path as per our requirements. Click on the ' New ' button since we want to add a new path.

**Step 5**: Paste the Path.

Paste the path of the MinGW bin that was copied earlier and click on `Ok`. Now if you repeat Step 9 you will see the version of the compiler in the cmd.

### Download a Source Code Editor

The source code editor is a text editor tool designed specially to edit or write the source code of any programming language. There is a basic source code editor present in Windows, i.e., Notepad, but it has limited features; therefore, for better formatting and features like multiple tabs, and plugins, you can use other editors like:


1.  Notepad++ (for Windows only): It is a text editor for Microsoft Windows. Unlike notepad, it supports multiple tabs.

2.  VS Code: (for Windows, Mac, and Linux) Visual Studio Code gives you suggestions to auto-complete the words. It has an inbuilt debugger to trace each line of code.

3.  ATOM: (for Windows, Mac, and Linux): Atom helps you write code faster with a smart and flexible autocomplete.


### Create and Run a C program

**Step 1**: Hello World in C.

To execute a C program, create a text file in any directory of your choice.

**Step 2**: Type the C code and Save the file.

Type the code in the notepad and save the file with the `.c` extension. Here we write a program to print _hello world_ to demonstrate this step and save the file as `Hello.c`.

```c
#include<stdio.h>

int main(){
  printf("Hello, World!")
  return o;
}
```

**Step 3**: Open Command Prompt.

Now, click on the address bar in the C program's directory, type `cmd`, and press Enter.

**Step 4**: Compile the C program.

To compile the Hello World code that we wrote earlier, type `gcc Hello.c` (or the name by which you will save the program) and press enter. Writing `gcc` will invoke the C compiler for windows.

**Step 5**: Compilation completed.

The compiled file will be saved in the same directory with the name _a_ (the name can be different for you). The type of the file will be _Application_.

**Step 6**: Running the C Program.

To run the compiled file, write the name of the compiled file, i.e., `a` and sthe output will be printed in the command prompt.

```
hello, world!
```
