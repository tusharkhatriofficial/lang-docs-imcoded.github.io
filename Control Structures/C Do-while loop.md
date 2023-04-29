<!-- 5-->
# C Do-while loop

A do-while loop is a loop statement used in C language that is used to execute a block of code repeatedly based on a given condition. The main difference between the do-while loop and the while loop is that the do-while loop guarantees at __least one execution of the code block__, while the while loop may not execute the code block at all if the condition is not satisfied.

__Syntax:__

The syntax of a do-while loop in C language is as follows:

```c
do {
    /* code block to be executed */
} while (condition);
```

__Working:__

When a do-while loop is encountered, the code block is executed once before checking the condition. After the execution of the code block, the condition is checked. If the condition is true, the code block is executed again, and the process repeats until the condition becomes false.

Let's look at an example:

```c
#include <stdio.h>

int main() {
    int i = 1;
    do {
        printf("%d ", i);
        i++;
    } while (i <= 10);
    return 0;
}
```

```zsh
1 2 3 4 5 6 7 8 9 10
```

In the above example, the do-while loop executes the code block once and prints the value of i, which is initially set to 1. After the first execution, the value of i is incremented by 1, and the condition is checked. Since the value of i is less than or equal to 10, the loop continues to execute, and the process repeats until the value of i becomes 11, at which point the condition becomes false, and the loop terminates.

<hr>

The do-while loop is a useful loop statement in C language that guarantees at least one execution of the code block. It is used in situations where we want to execute a block of code at least once, even if the condition is not initially satisfied.
