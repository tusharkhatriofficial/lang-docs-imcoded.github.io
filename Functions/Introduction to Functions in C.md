<!-- 1-->
In C, a function is a group of statements that perform a specific task. The task can be anything from performing a simple calculation to manipulating complex data structures. Functions have the following characteristics:



## What is a Function?

In C, a function is a group of statements that perform a specific task. The task can be anything from performing a simple calculation to manipulating complex data structures. Functions have the following characteristics:

- **Modularity:** Functions help to break down a program into smaller modules, which makes it easier to develop, debug and maintain.

- **Reuse:** Functions can be reused in different parts of the program, which saves time and effort in coding.

- **Efficiency:** Functions can help to improve the efficiency of the program, by allowing the program to call the function rather than repeating the same code multiple times.



## Syntax of Functions

```c
return_type function_name(parameter_list) {
   // Function body
   return value;
}
```

Where:

- `return_type` specifies the type of value that the function returns (e.g. int, float, etc.).
- `function_name` specifies the name of the function.
- `parameter_list` specifies the list of parameters that the function takes as input. If there are no parameters, the list is left empty.
- `function body` contains the statements that perform the task of the function.
- `return value` specifies the value that the function returns to the calling program.

## Steps to create and use a function in C

1. **Function Declaration:** The first step is to declare the function, which is essentially telling the compiler what the function will do, what input it will take, and what output it will give. This step is optional if you're defining the function before it's called in your program. The function declaration should include the function's return type, name, and parameter list. For example, let's declare a function named `sum` that takes two integers and returns an integer sum:

```c
int sum(int a, int b);
```

2. **Function Definition:** After declaring the function, you need to define the actual code that the function will execute when it's called. The function definition includes the function body, which is a block of code enclosed in curly braces `{}`. The code within the function body is executed when the function is called.

    For example, let's define the `sum` function that we declared earlier. The function definition will include the function body, where we add the two input integers and return the result:

```c
int sum(int a, int b) {
    int result = a + b;
    return result;
}
```

3. **Function Call:** Once you've declared and defined your function, you can call it in your program to execute the code within the function body. To call a function, you need to specify its name and pass in any required parameters. Here's an example of calling the `sum` function that we defined earlier:

```c
int x = 5;
int y = 7;
int z = sum(x, y);
printf("The sum of %d and %d is %d\n", x, y, z);
```

In the above example, we're calling the `sum` function and passing in two integers `x` and `y`. The function returns the sum of these integers, which is then stored in the variable `z`. Finally, we're using `printf` function to output the result to the console.

To get a better understanding let's look at an example of a function that calculates the sum of two numbers:

```c
#include <stdio.h>

// Function declaration
int sum(int a, int b);

int main() {
   int x = 5;
   int y = 10;
   int z = sum(x, y);//Function call
   printf("The sum of %d and %d is %d\n", x, y, z);
   return 0;
}

// Function definition
int sum(int a, int b) {
   int result = a + b;
   return result;
}
```

The `sum` function takes two integer parameters, adds them together and returns the result. The `main` function calls the `sum` function and assigns the result to the variable `z`. Finally, the program outputs the result to the console.