<!-- 3-->
# For loop

In programming, a loop is used to repeat a block of code until the specified condition is met.

C programming has three types of loops:

1.  for loop
2.  while loop
3.  do...while loop

A "for loop" is a control flow statement that allows us to execute a set of instructions repeatedly as long as a certain condition is met. The for loop in the C language is widely used to perform repetitive tasks. It provides an elegant and concise way to iterate over a block of code for a specific number of times.

Syntax: The syntax for a "for loop" in the C language is as follows:

```c
for (initialization; condition; increment) {
   statement(s);
}
```

where,

- `initialization` initializes the loop control variable, which is executed only once at the beginning of the loop.
- `condition` is a Boolean expression that is evaluated at the beginning of each iteration of the loop. If the condition is true, the statement(s) in the loop body are executed. If it is false, the loop terminates.
- `increment` is an expression that is executed after each iteration of the loop. It updates the loop control variable.
- `statement(s)` is the block of code that is executed repeatedly as long as the condition is true.

__Example 1:__

The following example demonstrates a simple "for loop" that prints the numbers from 1 to 5:

```c
#include <stdio.h>
int main() {
   int i;
   for (i = 1; i <= 5; i++) {
      printf("%d ", i);
   }
   return 0;
}
```

```zsh
1 2 3 4 5
```

__Explanation:__

- The variable `i` is initialized to 1 in the initialization statement.
- The condition checks if `i` is less than or equal to 5.
- The loop body prints the value of `i`.
- The increment statement updates the value of `i` by adding 1 to it.
- The loop continues until the value of `i` becomes greater than 5.

__Example 2:__

The following example demonstrates a "for loop" that prints the multiplication table of a number entered by the user:

```c
#include <stdio.h>
int main() {
   int num, i;
   printf("Enter a number: ");
   scanf("%d", &num);
   for (i = 1; i <= 10; i++) {
      printf("%d x %d = %d\n", num, i, num * i);
   }
   return 0;
}
```

```zsh
Enter a number: 5
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

__Explanation:__

- The user enters a number, which is stored in the variable `num`.
- The loop initializes the variable `i` to 1 and continues until `i` is less than or equal to 10.
- The loop body prints the multiplication table of `num` up to 10.
- The loop updates the value of `i` by adding 1 to it after each iteration.

__Example 3:__

The following example demonstrates a "for loop" that prints the sum of the first 10 natural numbers:

```c
#include <stdio.h>
int main() {
   int i, sum = 0;
   for (i = 1; i <= 10; i++) {
      sum += i;
   }
   printf("The sum of first 10 natural numbers is %d", sum);
   return 0;
}
```

```zsh
The sum of first 10 natural numbers is 55
```

__Explanation:__

- The loop initializes the variable `i` to 1 and continues until `i` is less than or equal to 10.
- The loop body adds the value of `i` to the variable `sum` in each iteration.
- After the loop completes, the variable `sum` contains the sum of the first 10 natural numbers.
- The printf statement prints the final value of the variable `sum`.

__Example 5:__

The following example demonstrates a "for loop" that prints a right triangle pattern of asterisks:

```c
#include <stdio.h>
int main() {
   int i, j, rows;
   printf("Enter the number of rows: ");
   scanf("%d", &rows);
   for (i = 1; i <= rows; i++) {
      for (j = 1; j <= i; j++) {
         printf("* ");
      }
      printf("\n");
   }
   return 0;
}
```

```zsh
Enter the number of rows: 5
*
* *
* * *
* * * *
* * * * *
```

__Explanation:__

- The user enters the number of rows for the triangle pattern, which is stored in the variable `rows`.
- The outer loop initializes the variable `i` to 1 and continues until `i` is less than or equal to `rows`.
- The inner loop initializes the variable `j` to 1 and continues until `j` is less than or equal to `i`.
- The inner loop body prints an asterisk and a space.
- The outer loop body prints a newline character after the inner loop completes, which creates a new row of asterisks in the triangle pattern.

<hr>

The "for loop" is a powerful tool in C programming that allows us to perform repetitive tasks efficiently. We can use it to iterate over arrays, print patterns, calculate sums, and perform many other tasks. By understanding the syntax and examples provided, you should be able to use for loops effectively in your programs.