# Even or Odd Number in C

## 📌 Description
This program checks whether a given integer is **Even** or **Odd**.

- An **Even number** is divisible by 2.
- An **Odd number** is not divisible by 2.

---

## ✨ Examples
10 → Even  
7  → Odd  

---

## 🧠 Algorithm
1. Read the input number.
2. Use the modulus operator (`%`) to check divisibility by 2.
3. If the remainder is 0, the number is Even.
4. Otherwise, the number is Odd.
5. Display the result.

---

## 💻 Program

#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Check even or odd */
    if (num % 2 == 0)
        printf("%d is an Even number.\n", num);
    else
        printf("%d is an Odd number.\n", num);

    return 0;
}
