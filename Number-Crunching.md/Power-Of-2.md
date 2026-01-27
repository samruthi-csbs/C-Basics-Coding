# Power of 2 in C

## 📌 Description
A number is said to be a **Power of 2** if it can be expressed in the form:

2ⁿ  (where n ≥ 0)

---

## ✨ Examples
1  → 2⁰ ✅  
2  → 2¹ ✅  
4  → 2² ✅  
8  → 2³ ✅  

10 → ❌ Not a Power of 2

---

## 🧠 Algorithm
1. Read the input number.
2. Check if the number is greater than 0.
3. Use the bitwise expression `(n & (n - 1))`.
4. If the result is 0, the number is a Power of 2.
5. Display the result.

---

## 💻 Program
#include <stdio.h>

/*
 A number is a Power of 2 if it can be written as 2^n
 where n is a non-negative integer.
 Example: 1, 2, 4, 8, 16, 32, ...
*/

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Check Power of 2 condition */
    if (num > 0 && (num & (num - 1)) == 0)
        printf("%d is a Power of 2.\n", num);
    else
        printf("%d is not a Power of 2.\n", num);

    return 0;
}
