# Check Ascending Order of Digits in C

## 📌 Description
This program checks whether the **digits of a given number are in ascending order**
(from left to right).

---

## ✨ Example
Input: 123459  
Output: Digits are in ascending order.

Input: 13245  
Output: Digits are not in ascending order.

---

## 🧠 Algorithm
1. Read the input number.
2. Convert it to positive if it is negative.
3. Extract digits from right to left.
4. Compare the current digit with the previous digit.
5. If any digit breaks ascending order, stop.
6. Print the result.

---

## 💻 Program





#include <stdio.h>

int main() {
    int num, prevDigit, currDigit;
    int isAscending = 1;

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

        if (currDigit > prevDigit) {
            isAscending = 0;
            break;
        }

        prevDigit = currDigit;
        num /= 10;
    }

    if (isAscending)
        printf("Digits are in ascending order.\n");
    else
        printf("Digits are not in ascending order.\n");

    return 0;
}
