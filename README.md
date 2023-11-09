
#include <stdio.h>

int main() {
    int password = 1234;
    int userPassword;
    
    printf("Enter the password: ");
    scanf("%d", &userPassword);

    if (userPassword != password) {
        printf("Incorrect password. Access denied.\n");
        return 1;
    }

    char operator;
    double num1, num2;

    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);

    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    double result;

    switch (operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if (num2 == 0) {
                printf("Division by zero is not allowed.\n");
                return 1;
            }
            result = num1 / num2;
            break;
        default:
            printf("Invalid operator.\n");
            return 1;
    }

    if (result >= 0) {
        printf("Result: %lf (Positive)\n", result);
    } else {
        printf("Result: %lf (Negative)\n", result);
    }

    return 0;
}
