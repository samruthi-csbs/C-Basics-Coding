# Count Occurrence of a Digit in C

## 📌 Description
This program counts how many times a **given digit occurs in a number**.

---

## ✨ Example
Number: 122333  
Digit: 3  

Occurrences: **3 times**

---

## 🧠 Algorithm
1. Read the number and the digit.
2. Convert the number to positive if it is negative.
3. Extract digits of the number using modulo (`%`).
4. Compare each digit with the given digit.
5. Increase the counter when a match is found.
6. Display the total count.

---

## 💻 Program






#include <stdio.h>

int main() {
    int num, digit, temp;
    int count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    printf("Enter the digit to count: ");
    scanf("%d", &digit);

    /* Handle negative numbers */
    if (num < 0) {
        num = -num;
    }

    temp = num;

    /* Count occurrence of the digit */
    while (temp > 0) {
        if (temp % 10 == digit) {
            count++;
        }
        temp /= 10;
    }

    printf("Digit %d occurs %d time(s) in the number.\n", digit, count);

    return 0;
}
