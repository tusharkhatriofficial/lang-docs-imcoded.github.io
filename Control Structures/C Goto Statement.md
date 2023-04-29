<!-- 8-->
# C Goto Statement

The Goto statement is a control flow statement in the C programming language that allows the programmer to transfer the program's control to a labeled statement within the same function. Although the Goto statement can be used to solve some programming problems, it is generally considered to be bad programming practice and should be used with caution.

The syntax of the Goto statement is as follows:

```c
goto label;
```

Here, label is the name of the labeled statement to which the control is transferred.

__Example:__

Here is an example of how to use the Goto statement in C:

```c
#include <stdio.h>

int main() {
   int i = 0;

   loop:
      printf("%d\n", i);
      i++;

      if (i < 10) {
         goto loop;
      }

   return 0;
}
```

In the above example, the Goto statement is used to transfer control to the labeled statement "loop" when the variable i is less than 10. The loop prints the value of i and increments it until i is greater than or equal to 10.

> It is recommended to use structured programming constructs such as loops, if statements, and switch statements instead of the Goto statement. Structured programming constructs make the program more readable, easier to understand, and less error-prone.