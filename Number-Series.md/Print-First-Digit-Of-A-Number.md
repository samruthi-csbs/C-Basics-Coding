# First Digit of a Number in C

## 📌 Description
This program finds and prints the **first digit** of a given integer.
It works for both **positive and negative numbers**.

---

## ✨ Example
Input: 4567  
Output: **4**

Input: -982  
Output: **9**

---

## 🧠 Algorithm
1. Read the input number.
2. Convert the number to positive if it is negative.
3. Repeatedly divide the number by 10 until it becomes a single digit.
4. Print that digit as the first digit.

---

## 💻 Program




#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Handle negative numbers */
    if (num < 0) {
        num = -num;
    }

    /* Find the first digit */
    while (num >= 10) {
        num /= 10;
    }

    printf("First digit = %d\n", num);

    return 0;
}
