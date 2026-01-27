# Spy Number in C

## 📌 Description
A **Spy Number** is a number in which the **sum of its digits**
is equal to the **product of its digits**.

---

## ✨ Example
123  
Sum of digits = 1 + 2 + 3 = 6  
Product of digits = 1 × 2 × 3 = 6 ✅  
So, 123 is a Spy Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Extract each digit.
3. Calculate the sum of digits.
4. Calculate the product of digits.
5. Compare sum and product.
6. Display the result.

---

## 💻 Program



#include <stdio.h>

/*
 A Spy Number is a number where the sum of its digits
 is equal to the product of its digits.
 Example: 112 -> sum = 1+1+2 = 4, product = 1*1*2 = 2 (Not Spy)
          123 -> sum = 1+2+3 = 6, product = 1*2*3 = 6 (Spy)
*/

int main() {
    int num, temp, digit;
    int sum = 0, product = 1;

    printf("Enter a number: ");
    scanf("%d", &num);

    temp = num;

    /* Calculate sum and product of digits */
    while (temp > 0) {
        digit = temp % 10;
        sum += digit;
        product *= digit;
        temp /= 10;
    }

    /* Check Spy Number condition */
    if (sum == product)
        printf("%d is a Spy Number.\n", num);
    else
        printf("%d is not a Spy Number.\n", num);

    return 0;
}
