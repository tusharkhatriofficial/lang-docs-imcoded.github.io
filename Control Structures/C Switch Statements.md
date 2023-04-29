<!-- 2-->
# Switch Statements

The **switch case statement** is used when we have multiple options and we need to perform a different task for each option. The switch statement is a conditional statement in C that allows you to test the value of a variable and execute different code blocks based on its value. It provides an efficient and concise way of writing conditional statements with multiple cases.

The switch statement allows us to execute one code block among many alternatives. You can do the same thing with the `if...else..if` ladder. However, the syntax of the `switch` statement is much easier to read and write.

Before we see how a switch case statement works in a C program, let’s checkout the syntax of it.

```c
switch (expression)
{
   case value1:
      // code to execute if the expression has the value of value1
      break;
   case value2:
      // code to execute if the expression has the value of value2
      break;
   ...
   default:
      // code to execute if the expression doesn't match any of the cases
      break;
}
```

Here, the expression is the variable or expression that you want to test, and the case labels specify the values that you want to test for. The default label is optional and specifies the code to execute if none of the cases match.

**Examples**

Let's take a look at some examples of using the switch statement:

```c
#include <stdio.h>

int main()
{
   char operator;
   double num1, num2, result;

   printf("Enter an operator (+, -, *, /): ");
   scanf("%c", &operator);

   printf("Enter two operands: ");
   scanf("%lf %lf", &num1, &num2);

   switch (operator)
   {
      case '+':
         result = num1 + num2;
         printf("%.2lf + %.2lf = %.2lf\n", num1, num2, result);
         break;
      case '-':
         result = num1 - num2;
         printf("%.2lf - %.2lf = %.2lf\n", num1, num2, result);
         break;
      case '*':
         result = num1 * num2;
         printf("%.2lf * %.2lf = %.2lf\n", num1, num2, result);
         break;
      case '/':
         if (num2 == 0)
         {
            printf("Error: Division by zero\n");
         }
         else
         {
            result = num1 / num2;
            printf("%.2lf / %.2lf = %.2lf\n", num1, num2, result);
         }
         break;
      default:
         printf("Error: Invalid operator\n");
         break;
   }

   return 0;
}
```

In this example, the switch statement is used to perform different arithmetic operations based on the value of the operator variable. The user is prompted to enter an operator (+, -, *, /) and two operands, and the switch statement tests the value of the operator variable and performs the corresponding operation.

Another example of using the switch statement:

The switch statement can be used to display the name of a month based on the value of a variable. Consider the following program that prompts the user to enter a month number (1-12) and displays the corresponding month name using the switch statement:

```c
#include <stdio.h>

int main()
{
   int month;

   printf("Enter a month number (1-12): ");
   scanf("%d", &month);

   switch (month)
   {
      case 1:
         printf("January\n");
         break;
      case 2:
         printf("February\n");
         break;
      case 3:
         printf("March\n");
         break;
      case 4:
         printf("April\n");
         break;
      case 5:
         printf("May\n");
         break;
      case 6:
         printf("June\n");
         break;
      case 7:
         printf("July\n");
         break;
      case 8:
         printf("August\n");
         break;
      case 9:
         printf("September\n");
         break;
      case 10:
         printf("October\n");
         break;
      case 11:
         printf("November\n");
         break;
      case 12:
         printf("December\n");
         break;
      default:
         printf("Error: Invalid month number\n");
         break;
   }

   return 0;
}
```

In this example, the switch statement is used to display the name of the month based on the value of the month variable. The user is prompted to enter a month number (1-12), and the switch statement tests the value of the month variable and displays the corresponding month name.

The switch statement starts with the keyword "switch" followed by the variable or expression that we want to test. In this case, it is the "month" variable that holds the value entered by the user. We then have a series of "case" statements that specify the different values that we want to test for. Each case statement is followed by a colon and the code that we want to execute if the value matches the case.

For example, the first case statement checks if the value of the month variable is 1, and if it is, it prints "January" followed by a newline character. The "break" statement at the end of each case is important because it tells the program to exit the switch statement and continue with the rest of the program.

The "default" case is optional and is executed if none of the other cases match the value of the variable. In this case, if the user enters a value that is not between 1 and 12, the program prints an error message.

