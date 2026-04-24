### C PROGRAM ASSIGNMENT
## NAME: SARAVANAN P
## REG NO:212224230353



 1. Write a C program to find the maximum of three numbers without using logical operators.
```
#include <stdio.h>

int main() {
    int a, b, c, max;

    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);

    max = a;

    if (b > max)
        max = b;

    if (c > max)
        max = c;

    printf("Maximum = %d", max);

    return 0;
}
```
##  output
<img width="1866" height="1150" alt="image" src="https://github.com/user-attachments/assets/42b8afdc-a78d-46e4-bfe4-ad9865818a95" />


2. Write a C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)
```
#include <stdio.h>

int main() {
    int year;

    printf("Enter year: ");
    scanf("%d", &year);

    if (year % 400 == 0) {
        printf("%d is a Century Leap Year", year);
    }
    else if (year % 100 == 0) {
        printf("%d is a Century Non-Leap Year", year);
    }
    else if (year % 4 == 0) {
        printf("%d is a Non-Century Leap Year", year);
    }
    else {
        printf("%d is Not a Leap Year", year);
    }

    return 0;
}
```
## output
<img width="1866" height="1105" alt="image" src="https://github.com/user-attachments/assets/720f5254-b3b9-439d-ad2a-1a3a801f8bef" />

3. Write a C program to find whether the entered character is alphabet / digit / special character. If the entered character is an alphabet then say it is vowel or consonant without 
using built in functions
```
#include <stdio.h>

int main() {
    char ch;

    printf("Enter a character: ");
    scanf(" %c", &ch);

    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z')) {

        printf("Alphabet\n");

        if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||
            ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U') {
            printf("Vowel");
        } else {
            printf("Consonant");
        }

    }
    else if (ch >= '0' && ch <= '9') {
        printf("Digit");
    }
    else {
        printf("Special Character");
    }

    return 0;
}

```
## output

<img width="1863" height="1101" alt="image" src="https://github.com/user-attachments/assets/5c5db5d5-018b-4825-9ace-2b242b715139" />

4. Write a C program for simple ATM simulation with operations Check Balance, Deposit, Withdraw, Exit using switch and update balance accordingly.
```

#include <stdio.h>

int main() {
    int choice;
    float balance = 1000, amount;

    do {
        printf("\n1. Check Balance\n2. Deposit\n3. Withdraw\n4. Exit\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Balance = %.2f\n", balance);
                break;

            case 2:
                printf("Enter amount to deposit: ");
                scanf("%f", &amount);
                balance += amount;
                printf("Updated Balance = %.2f\n", balance);
                break;

            case 3:
                printf("Enter amount to withdraw: ");
                scanf("%f", &amount);
                if (amount <= balance) {
                    balance -= amount;
                    printf("Updated Balance = %.2f\n", balance);
                } else {
                    printf("Insufficient Balance\n");
                }
                break;

            case 4:
                printf("Thank you!\n");
                break;

            default:
                printf("Invalid choice\n");
        }

    } while (choice != 4);

    return 0;
}
```
## output

<img width="1868" height="1149" alt="image" src="https://github.com/user-attachments/assets/87e551d0-6138-4de9-8c3f-b826e646d64a" />

5. Write a C program for menu driven calculator using switch statement.
```
#include <stdio.h>

int main() {
    int choice;
    float a, b;

    printf("Enter two numbers: ");
    scanf("%f %f", &a, &b);

    printf("\n1.Add\n2.Subtract\n3.Multiply\n4.Divide\n");
    printf("Enter choice: ");
    scanf("%d", &choice);

    switch (choice) {
        case 1:
            printf("Result = %.2f", a + b);
            break;

        case 2:
            printf("Result = %.2f", a - b);
            break;

        case 3:
            printf("Result = %.2f", a * b);
            break;

        case 4:
            if (b != 0)
                printf("Result = %.2f", a / b);
            else
                printf("Division by zero error");
            break;

        default:
            printf("Invalid choice");
    }

    return 0;
}
```
## output
<img width="1865" height="1104" alt="image" src="https://github.com/user-attachments/assets/962b7b42-61ff-49ed-8a69-73fb784c9b02" />
