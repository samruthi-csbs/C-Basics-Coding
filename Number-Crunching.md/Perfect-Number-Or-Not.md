# Perfect Number in C

## 📌 Description
A **Perfect Number** is a positive integer that is equal to the **sum of its proper divisors**
(excluding the number itself).

---

## ✨ Example
6  
Divisors: 1, 2, 3  
Sum = 1 + 2 + 3 = **6** ✅  
So, 6 is a Perfect Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Find all divisors from 1 to n/2.
3. Add the divisors.
4. Compare the sum with the original number.
5. Display the result.







#include <stdio.h>

int main() {
    int num, i, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Calculate sum of proper divisors */
    for (i = 1; i <= num / 2; i++) {
        if (num % i == 0) {
            sum += i;
        }
    }

    /* Check Perfect Number condition */
    if (sum == num && num != 0)
        printf("%d is a Perfect Number.\n", num);
    else
        printf("%d is not a Perfect Number.\n", num);

    return 0;
}
