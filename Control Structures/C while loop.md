<!-- 4-->
# C while loop

In the previous tutorial, we learned about `for` loop. In this tutorial, we will learn about `while`  loop.

A while loop is a control structure in the C programming language that allows a programmer to execute a block of code repeatedly while a certain condition is true. The while loop consists of a condition and a block of code that will be executed repeatedly as long as the condition is true. In this tutorial, we will discuss the syntax of the while loop, how it works, and provide various examples to illustrate its usage.

__Syntax:__

The syntax for the while loop in C programming language is as follows:

```c
while (condition) {
   statement(s);
}
```

The while loop starts with the keyword `while` followed by a condition in parentheses. The condition is a boolean expression that evaluates to true or false. If the condition is true, the block of code inside the while loop will be executed. After executing the code, the condition is checked again. If it is still true, the code is executed again. This process continues until the condition becomes false.

__Example 1:__

```c
#include <stdio.h>

int main() {
   int i = 1;

   while (i <= 10) {
      printf("%d ", i);
      i++;
   }
   
   return 0;
}
```

```zsh
1 2 3 4 5 6 7 8 9 10
```

In this example, we have initialized a variable `i` to 1. We have used a while loop to print the numbers from 1 to 10. The condition `i <= 10` is true for values of i from 1 to 10. Inside the while loop, we have used the printf() function to print the value of i. We have then incremented the value of i by 1 using the `i++` statement. This process continues until the value of i becomes 11, at which point the condition becomes false and the loop terminates.

__Example 2:__

```c
#include <stdio.h>

int main() {
   int num;

   printf("Enter a positive integer: ");
   scanf("%d", &num);

   while (num < 0) {
      printf("Error: Enter a positive integer: ");
      scanf("%d", &num);
   }

   printf("You entered: %d", num);

   return 0;
}
```

```zsh
Enter a positive integer: -5
Error: Enter a positive integer: -3
Error: Enter a positive integer: 0
Error: Enter a positive integer: 10
You entered: 10
```

In the above example, we have used a while loop to ask the user to enter a positive integer. The loop will continue to execute as long as the user enters a negative number. Inside the loop, we have printed an error message asking the user to enter a positive integer. We have then used the scanf() function to read the input from the user and store it in the `num` variable. This process continues until the user enters a positive integer, at which point the loop terminates and the program prints the value of `num`.

__Example 3:__

```c
#include <stdio.h>

int main() {
   int i = 10;

   while (i > 0) {
      printf("%d ", i);
      i -= 2;
   }

   return 0;
}
```

```zsh
10 8 6 4 2
```

In the above example, we have initialized the variable `i` to 10. Inside the while loop, we have used the printf() function to print the value of `i`. We have then decremented the value of `i` by 2 using the `i -= 2` statement. This process continues until the value of `i` becomes 0, at which point the condition becomes false and the loop terminates.

__Example 4:__

```c
#include <stdio.h>

int main() {
   int num, sum = 0;

   printf("Enter numbers to add up. Enter 0 to stop.\n");

   while (1) {
      scanf("%d", &num);
      if (num == 0) {
         break;
      }
      sum += num;
   }

   printf("The sum is: %d", sum);

   return 0;
}
```

```zsh
Enter numbers to add up. Enter 0 to stop.
5
10
15
0
The sum is: 30
```

In the above example, we have used a while loop to add up a list of numbers entered by the user. The loop will continue to execute until the user enters 0. Inside the loop, we have used the scanf() function to read the input from the user and store it in the `num` variable. We have then used an if statement to check if the value of `num` is 0. If it is, we have used the `break` statement to terminate the loop. If it is not 0, we have added the value of `num` to the `sum` variable. This process continues until the user enters 0, at which point the loop terminates and the program prints the value of `sum`.

<hr>

The while loop is a powerful control structure in the C programming language that allows a programmer to execute a block of code repeatedly while a certain condition is true. The syntax of the while loop is simple, and it can be used in a wide variety of applications. By using the examples provided in this tutorial, you should be able to understand how to use the while loop in your own programs.

