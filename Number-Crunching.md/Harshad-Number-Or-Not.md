# Harshad Number in C

## 📌 Description
A **Harshad Number** (also called a **Niven Number**) is an integer that is
**divisible by the sum of its digits**.

---

## ✨ Example
18  
Sum of digits = 1 + 8 = 9  
18 ÷ 9 = 2 ✅  
So, 18 is a Harshad Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Extract each digit and calculate their sum.
3. Check if the number is divisible by the sum of its digits.
4. Print the result.










#include <stdio.h>

int main() {
    int num, temp, digit;
    int sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    temp = num;

    /* Calculate sum of digits */
    while (temp > 0) {
        digit = temp % 10;
        sum += digit;
        temp /= 10;
    }

    /* Check Harshad Number condition */
    if (sum != 0 && num % sum == 0)
        printf("%d is a Harshad Number.\n", num);
    else
        printf("%d is not a Harshad Number.\n", num);

    return 0;
}
