# Digit Occurrence in a Number (C)

## 📌 Description
This program checks whether a **given digit occurs in a number**.

---

## ✨ Example
Number: 75843  
Digit: 8  

Output: **Digit 8 is present in the number.**

---

## 🧠 Algorithm
1. Read the number and the digit.
2. Convert the number to positive if it is negative.
3. Extract digits of the number using modulo (`%`).
4. Compare each digit with the given digit.
5. If a match is found, stop and print the result.

---

## 💻 Program


#include <stdio.h>

int main() {
    int num, digit, temp;
    int found = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    printf("Enter the digit to check: ");
    scanf("%d", &digit);

    /* Handle negative numbers */
    if (num < 0) {
        num = -num;
    }

    temp = num;

    /* Check occurrence of digit */
    while (temp > 0) {
        if (temp % 10 == digit) {
            found = 1;
            break;
        }
        temp /= 10;
    }

    if (found)
        printf("Digit %d is present in the number.\n", digit);
    else
        printf("Digit %d is not present in the number.\n", digit);

    return 0;
}
