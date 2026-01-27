# Neon Number in C

## 📌 Description
A **Neon Number** is a number where the **sum of the digits of its square**
is equal to the original number.

---

## ✨ Example
9  
Square = 9 × 9 = 81  
Sum of digits = 8 + 1 = **9** ✅  
So, 9 is a Neon Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Find the square of the number.
3. Extract digits of the square.
4. Add the digits.
5. Compare the sum with the original number.
6. Print the result.









#include <stdio.h>

int main() {
    int num, square, sum = 0, digit;

    printf("Enter a number: ");
    scanf("%d", &num);

    square = num * num;

    /* Calculate sum of digits of the square */
    while (square > 0) {
        digit = square % 10;
        sum += digit;
        square /= 10;
    }

    /* Check Neon Number condition */
    if (sum == num)
        printf("%d is a Neon Number.\n", num);
    else
        printf("%d is not a Neon Number.\n", num);

    return 0;
}
