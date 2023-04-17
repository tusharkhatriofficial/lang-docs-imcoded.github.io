<!-- 5-->
# Operators

Operators are an essential part of any programming language, including C. They are symbols that instruct the compiler to perform specific arithmetic or logical operations on the operands. C programming language provides a wide range of operators, which can be classified into different categories.



## Arithmetic Operators:

Arithmetic operators are used to perform mathematical operations on numerical operands. The following are the arithmetic operators in C:

- Addition (+)
- Subtraction (-)
- Multiplication (*)
- Division (/)
- Modulus (%)

| Operator | Meaning of Operator                        |
|----------|--------------------------------------------|
| +        | addition or unary plus                     |
| -        | subtraction or unary minus                 |
| *        | multiplication                             |
| /        | division                                   |
| %        | remainder after division (modulo division) |


```c
#include <stdio.h>

int main() {
   int a = 10, b = 5;
   
   printf("Addition: %d\n", a + b);
   printf("Subtraction: %d\n", a - b);
   printf("Multiplication: %d\n", a * b);
   printf("Division: %d\n", a / b);
   printf("Modulus: %d\n", a % b);
   
   return 0;
}
```

```zsh
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2
Modulus: 0
```


The operators `+`, `-` and `*` computes addition, subtraction, and multiplication respectively as you might have expected.

The `/` operator will always return an integer value if both the operands are integers so if `a=9` and `b=5` the answer must be 1.8 but the compiler will return 1.

```c
#include <stdio.h>

int main() {
   int a = 9, b = 5;
   printf("Division: %d\n", a / b);
   return 0;
}
```

```zsh
Division: 1
```

The modulo operator `%` computes the remainder. When `a=10` is divided by `b=5`, the remainder is `0`. The `%` operator can only be used with integers.



## Increment and Decrement Operators

C language provides two unary operators known as increment and decrement operators, which can be used to increase or decrease the value of a variable by 1. These operators are represented by "++" and "--" respectively. They are commonly used in loop constructs and expressions where the value of a variable needs to be incremented or decremented.


### Increment Operator (++)

The increment operator is used to increase the value of a variable by 1. It can be used in two ways: as a postfix operator or as a prefix operator.

- __Postfix Increment Operator__

  The postfix increment operator "++" increases the value of the variable after the expression is evaluated. It is used in the following way:

```c
int x = 5;
int y = x++;
```

  In this example, the value of `x` is first assigned to `y`, and then `x` is incremented by 1. Therefore, the value of `y` is 5, and the value of `x` is 6.
  
  - __Prefix Increment Operator__

  The prefix increment operator "++" increases the value of the variable before the expression is evaluated. It is used in the following way:

```c
int x = 5;
int y = ++x;
```

  In this example, `x` is incremented by 1, and then its value is assigned to `y`. Therefore, the value of `y` is 6, and the value of `x` is also 6.


### Decrement Operator (--)

The decrement operator is used to decrease the value of a variable by 1. It can also be used as a postfix operator or a prefix operator.

- __Postfix Decrement Operator__

  The postfix decrement operator "--" decreases the value of the variable after the expression is evaluated. It is used in the following way:
  
```c
int x = 5;
int y = x--;
```

  In this example, the value of `x` is first assigned to `y`, and then `x` is decremented by 1. Therefore, the value of `y` is 5, and the value of `x` is 4.

- __Prefix Decrement Operator__

  The prefix decrement operator "--" decreases the value of the variable before the expression is evaluated. It is used in the following way:

```c
int x = 5;
int y = --x;
```

In this example, `x` is decremented by 1, and then its value is assigned to `y`. Therefore, the value of `y` is 4, and the value of `x` is also 4.



## Assignment Operators:

Assignment operators are used to assign values to variables. The following are the assignment operators in C:

-   Assignment (=)
-   Addition assignment (+=)
-   Subtraction assignment (-=)
-   Multiplication assignment (*=)
-   Division assignment (/=)
-   Modulus assignment (%=)

The assignment operator, denoted by the "=" symbol, is used to assign a value to a variable. The basic syntax of the assignment operator is:

```zsh
variable = value;
```

Here, the variable is the name of the variable to which the value will be assigned, and the value is the expression whose value will be assigned to the variable.

For example, consider the following code snippet:

```c
int x = 10;
int y;
y = x;
```

In this code, the variable "x" is assigned the value of 10 using the initialization syntax. The variable "y" is declared without an initial value, and then the value of "x" is assigned to it using the assignment operator.

Another example:

```c
float a = 5.0;
float b = 2.0;
float c = a / b;
```

In this code, the variables "a" and "b" are initialized with the values 5.0 and 2.0, respectively. The expression "a / b" is evaluated and the resulting value is assigned to the variable "c" using the assignment operator.

> It is important to note that the assignment operator only assigns the value to the variable on the left-hand side of the operator. The expression on the right-hand side is evaluated first, and then the resulting value is assigned to the variable on the left-hand side.

The assignment operator can be combined with other operators to create compound assignment operators. For example, the following code is equivalent to "x = x + 5":

```c
x += 5;
```

The "+=" operator adds the value on the right-hand side to the value of the variable on the left-hand side, and then assigns the resulting value back to the variable on the left-hand side.

The blow given example contains all the assignment operators listed above:

```c
#include <stdio.h>

int main() {
    int x = 10;
    int y = 5;
    
    // Assignment
    int a = x;
    
    // Addition assignment
    int b = y;
    b += x;
    
    // Subtraction assignment
    int c = y;
    c -= x;
    
    // Multiplication assignment
    int d = y;
    d *= x;
    
    // Division assignment
    int e = x;
    e /= y;
    
    // Modulus assignment
    int f = x;
    f %= y;
    
    printf("a = %d\n", a);
    printf("b = %d\n", b);
    printf("c = %d\n", c);
    printf("d = %d\n", d);
    printf("e = %d\n", e);
    printf("f = %d\n", f);
    
    return 0;
}
```

In this code, we initialize the variables "x" and "y" with the values 10 and 5, respectively. We then use each of the different types of assignment operators to perform operations on these variables and store the results in different variables ("a" through "f").

```zsh
a = 10
b = 15
c = -5
d = 50
e = 2
f = 0
```

As you can see, each assignment operator performs a different operation and produces a different result. The addition assignment adds the value on the right-hand side to the value of the variable on the left-hand side, the subtraction assignment subtracts the value on the right-hand side from the value of the variable on the left-hand side, and so on. The modulus assignment calculates the remainder when the variable on the left-hand side is divided by the value on the right-hand side.
