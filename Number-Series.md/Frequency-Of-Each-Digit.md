# Frequency of a Digit in C

## 📌 Description
This program finds the **frequency (number of times)** a given digit
occurs in a given number.

---

## ✨ Example
Number: 122334  
Digit: 2  

Frequency = **2**

---

## 🧠 Algorithm
1. Read the number.
2. Read the digit whose frequency is needed.
3. Extract digits of the number using `% 10`.
4. Compare each digit with the given digit.
5. Increase count when matched.
6. Print the frequency.

---

## 💻 Program





#include <stdio.h>

int main() {
    int num, digit, temp, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    printf("Enter the digit to find frequency: ");
    scanf("%d", &digit);

    /* Make number positive if negative */
    if (num < 0)
        num = -num;

    temp = num;

    /* Count frequency of digit */
    while (temp > 0) {
        if (temp % 10 == digit) {
            count++;
        }
        temp = temp / 10;
    }

    printf("Frequency of %d is %d\n", digit, count);

    return 0;
}
