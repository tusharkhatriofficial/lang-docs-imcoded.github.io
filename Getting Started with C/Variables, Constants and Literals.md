<!-- 3-->
# C Variables, Constants and Literals

In this tutorial, you will learn about variables, constants, and literals in C programming language. By understanding how to use variables, constants, and literals effectively, you can create powerful and flexible programs in C. You will learn how to declare and initialize variables, how to define constants, and how to work with different types of literals.



## Variables

A variable is a storage location in a computer's memory where a value can be stored and retrieved. In C programming language, you need to declare a variable before using it in the program. Declaring a variable involves specifying the variable type and a name for the variable.

```c
int age; // Declaring an integer variable named age
```

Here, `int` is the variable type, and `age` is the variable name. The `int` type is used to store integers.

You can assign a value to a variable using the assignment operator `=`.

```c
int age;
age = 20; // Assigning the value 25 to the age variable
```

You can also declare and initialize a variable in a single statement.

```c
int age = 20; // Declaring and initializing the age variable with the value 20
```

### Rules for naming a variable

- A variable name can only have letters (both uppercase and lowercase letters), digits and underscore.

- The first letter of a variable should be either a letter or an underscore.

- There is no rule on how long a variable name (identifier) can be. However, you may run into problems in some compilers if the variable name is longer than 31 characters.

> It's important to use consistent naming conventions when declaring variables. For instance, if you're using camelCase to name your variables (e.g. `firstName`, `lastName`), you should stick to that convention throughout your code. This makes your code more readable and easier to understand. Mixing different naming conventions (e.g. using camelCase for some variables and snake_case for others) can make your code harder to read and maintain, especially if you're working with other developers. So, it's best to pick a convention and stick to it.



## Constants

A constant is a value that cannot be changed during the execution of the program. In C programming language, you can define a constant using the `const` keyword.

```c
const int max_num = 100; // Declaring a constant named MAX_NUM with the value 100
```

In this example, `max_num` is the name of the constant, and `const int` is the constant type. The `const` keyword ensures that the value of the constant cannot be changed during the execution of the program.



## Literals

In computer programming, a literal is a value that is explicitly specified in the source code of the program. In other words, it is a fixed value that is "literally" present in the code.

For example, in the following C code, `20` is an integer literal and `"Tushar Khatri"` is a string literal:

```c
int age = 20;
char greeting[] = "Tushar Khatri";
```

There are several types of literals in C programming language, including integer literals, floating-point literals, character literals, and string literals. These different types of literals allow you to represent different kinds of values in your code.

### Integer Literals

An integer literal is a numeric value that does not contain a decimal point.

```c
int num = 10; // Declaring an integer variable named num with the value 10
```

### Floating-Point Literals

A floating-point literal is a numeric value that contains a decimal point.

```c
float pi = 3.14; // Declaring a float variable named pi with the value 3.14
```

### Character Literals

A character literal is a single character enclosed in single quotes.

```c
char ch = 'A'; // Declaring a character variable named ch with the value 'A'
```

### String Literals

A string literal is a sequence of characters enclosed in double quotes.

```c
char str[] = "why do submarines all run Linux :)"; // Declaring a character array variable named str with the value "why do submarines all run Linux :)"
```



Variables, Constants, and Literals are essential concepts that you need to understand when programming in C. By using these concepts effectively, you can create powerful and flexible programs in C.