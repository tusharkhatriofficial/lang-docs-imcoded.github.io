<!-- 4-->
# Typecasting

Typecasting, also known as type conversion, is the process of converting a value from one data type to another. In C programming language, there are two types of typecasting: implicit typecasting (also known as coercion) and explicit typecasting.



## Implicit typecasting

Implicit typecasting happens automatically when the compiler converts one data type to another without any explicit indication from the programmer. This happens when you assign a value of one data type to a variable of a different data type. For example:

```c
int num = 10;
float num_f = num; // implicit typecasting
```

we assign the integer value 10 to the variable `num`, and then assign the value of `num` to a float variable named `num_f`. Since `num` is an integer and `num_f` is a float, implicit typecasting occurs, and `num` is automatically converted to a float.



# Explicit typecasting

Explicit typecasting, on the other hand, is when the programmer explicitly indicates that a value should be converted from one data type to another. This is done by placing the data type to which the value should be converted in parentheses before the value. For example:

```c
int num = 10;
float num_f = (float) num; // explicit typecasting
```

In the example above, we use explicit typecasting to convert the value of `num` to a float. The `(float)` before `num` indicates that `num` should be converted to a float before being assigned to `num_f`.

Here are a few more examples of how to use typecasting in C programming language:


### Converting an Integer to a Character

```c
int num = 82; // ASCII code for capital letter A
char ch = (char) num; // explicit typecasting
printf("%c", ch); // Output: A
```

we used explicit typecasting to convert the integer value 82 to a character. The `(char)` before `num` indicates that `num` should be converted to a character before being assigned to `ch`. The `printf()` function is then used to output the value of `ch`.


### Converting a Floating-Point Number to an Integer

```c
float num_f = 3.14;
int num = (int) num_f; // explicit typecasting
printf("%d", num); // Output: 3
```

we used explicit typecasting to convert the floating-point value 3.14 to an integer. The `(int)` before `num_f` indicates that `num_f` should be converted to an integer before being assigned to `num`. The `printf()` function is then used to output the value of `num`.


### Converting a String to an Integer

```c
char str[] = "25182";
int num = atoi(str); // explicit typecasting using atoi() function
printf("%d", num); // Output: 25182
```

In this example, we use the `atoi()` function to explicitly convert the string "25182" to an integer. The `atoi()` function takes a string as input and returns an integer. The value returned by `atoi()` is then assigned to the variable `num`, which is then outputted using the `printf()` function.

Finally, Typecasting is an important concept in C programming language that allows you to convert values from one data type to another. Implicit typecasting happens automatically, while explicit typecasting requires the programmer to explicitly indicate the desired data type using parentheses. Understanding how to use typecasting effectively can help you create more flexible and powerful programs.
