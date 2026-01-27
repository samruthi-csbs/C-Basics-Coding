# Check Descending Order of Digits in C

## 📌 Description
This program checks whether the **digits of a given number are in descending order**
(from left to right).

---

## ✨ Example
Input: 97531  
Output: Digits are in descending order.

Input: 95421  
Output: Digits are not in descending order.

---

## 🧠 Algorithm
1. Read the input number.
2. Convert it to positive if it is negative.
3. Extract digits from right to left.
4. Compare each digit with the previous digit.
5. If any digit breaks descending order, stop.
6. Print the result.

---

## 💻 Program








#include <stdio.h>

int main() {
    int num, prevDigit, currDigit;
    int isDescending = 1;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Handle negative numbers */
    if (num < 0) {
        num = -num;
    }

    prevDigit = num % 10;
    num /= 10;

    /* Check digits from right to left */
    while (num > 0) {
        currDigit = num % 10;

        if (currDigit < prevDigit) {
            isDescending = 0;
            break;
        }

        prevDigit = currDigit;
        num /= 10;
    }

    if (isDescending)
        printf("Digits are in descending order.\n");
    else
        printf("Digits are not in descending order.\n");

    return 0;
}
