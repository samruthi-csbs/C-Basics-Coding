# Prime Number Checker in C

A simple C program to check whether a given number is a **prime number** or not.  

This project is perfect for beginners learning C programming and understanding basic concepts like loops, conditionals, and input/output.

---

## Features

- Checks if a single number is prime
- Handles edge cases like 0, 1, and negative numbers
- Simple and easy-to-understand code
####(The C Program)





#include <stdio.h>

int main() {
    int num, i, isPrime = 1;

    // Ask user for input
    printf("Enter a number: ");
    scanf("%d", &num);

    if (num <= 1) {
        isPrime = 0; // 0 and 1 are not prime
    } else {
        for (i = 2; i * i <= num; i++) {
            if (num % i == 0) {
                isPrime = 0;
                break;
            }
        }
    }

    if (isPrime)
        printf("%d is a prime number.\n", num);
    else
        printf("%d is not a prime number.\n", num);

    return 0;
}
