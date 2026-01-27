# Buzz Number in C

## 📌 Description
A **Buzz Number** is a number that:
- is divisible by **7**, OR
- ends with the digit **7**

If either condition is satisfied, the number is called a Buzz Number.

---

## ✨ Example
14  
14 ÷ 7 = 2 ✅  
So, 14 is a Buzz Number.

27  
Ends with digit 7 ✅  
So, 27 is a Buzz Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Check if the number is divisible by 7.
3. Check if the last digit of the number is 7.
4. If either condition is true, it is a Buzz Number.
5. Print the result.









#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* A Buzz number is divisible by 7 or ends with 7 */
    if (num % 7 == 0 || num % 10 == 7)
        printf("%d is a Buzz Number.\n", num);
    else
        printf("%d is not a Buzz Number.\n", num);

    return 0;
}
