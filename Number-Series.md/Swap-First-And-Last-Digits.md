# Swap First and Last Digit of a Number (C)

## 📌 Description
This program swaps the **first digit** and the **last digit** of a given integer.

---

## ✨ Example
Input: 1234  
Output: **4231**

Input: 9087  
Output: **7089**

---

## 🧠 Algorithm
1. Read the input number.
2. Extract the last digit using modulo (`% 10`).
3. Find the total number of digits using `log10`.
4. Extract the first digit using division.
5. Construct the new number by swapping the first and last digits.
6. Display the result.

---

## 💻 Program








#include <stdio.h>
#include <math.h>

int main() {
    int num, temp, firstDigit, lastDigit, digits;
    int swappedNum;

    printf("Enter a number: ");
    scanf("%d", &num);

    temp = num;
    lastDigit = temp % 10;

    /* Count number of digits */
    digits = (int)log10(temp);

    /* Get first digit */
    firstDigit = temp / (int)pow(10, digits);

    /* Swap first and last digits */
    swappedNum = lastDigit * pow(10, digits)
               + (temp % (int)pow(10, digits)) / 10 * 10
               + firstDigit;

    printf("Number after swapping first and last digit: %d\n", swappedNum);

    return 0;
}
