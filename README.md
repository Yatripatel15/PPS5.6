# PPS5.6
Write a simple calculator program performing all five basic operations 
#include <stdio.h>

int main() 
{
    char operator;
    int a, b, c;

    // Take user input for the two numbers
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    // Take user input for the operator
    printf("Enter an operator (+, -, *, /, %%): ");
    scanf(" %c", &operator);

    // Using if to check for valid operators
    if (operator == '+' || operator == '-' || operator == '*' || operator == '/' || operator == '%') 
    {

        // Using switch to perform the calculation
        switch (operator) 
        {
            case '+':
                c = a + b;
                printf("%d + %d = %d\n", a, b, c);
                break;

            case '-':
                c = a - b;
                printf("%d - %d = %d\n", a, b, c);
                break;

            case '*':
                c= a * b;
                printf("%d * %d = %d\n", a, b, c);
                break;

            case '/':
                if (b != 0) 
                {
                    c= a / b;
                    printf("%d / %d = %d\n", a, b, c);
                } 
              
                break;

            case '%':
                if (b != 0) 
                {
                    c = a % b;
                    printf("%d %% %d = %d\n", a, b, c);
                } 
                break;
        }

    } 
    

    return 0;
}

