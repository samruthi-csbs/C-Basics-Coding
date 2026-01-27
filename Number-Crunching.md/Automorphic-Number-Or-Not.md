# Automorphic Number in C

## 📌 Description
An **Automorphic Number** is a number whose **square ends with the same digits**
as the number itself.

---

## ✨ Example
25  
Square = 25 × 25 = 625  
Last two digits = **25** ✅  
So, 25 is an Automorphic Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Find the square of the number.
3. Count the number of digits in the original number.
4. Compute 10 raised to the power of number of digits.
5. Compare the last digits of the square with the original number.
6. Display the result.

---

## 💻 Program




#include <stdio.h>

int main() {
    int num, square;
    int temp, digits = 0;
    int power = 1;

    printf("Enter a number: ");
    scanf("%d", &num);

    square = num * num;
    temp = num;

    /* Count number of digits in the number */
    while (temp > 0) {
        digits++;
        temp /= 10;
    }

    /* Calculate 10^digits */
    for (int i = 0; i < digits; i++) {
        power *= 10;
    }

    /* Check Automorphic condition */
    if (square % power == num)
        printf("%d is an Automorphic Number.\n", num);
    else
        printf("%d is not an Automorphic Number.\n", num);

    return 0;
}
