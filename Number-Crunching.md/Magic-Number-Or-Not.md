# Magic Number in C

## 📌 Description
A **Magic Number** is a number in which the **sum of its digits is repeatedly
calculated until a single digit is obtained**, and that final digit is **1**.

---

## ✨ Example
19  
1 + 9 = 10  
1 + 0 = **1** ✅  
So, 19 is a Magic Number.

---

## 🧠 Algorithm
1. Read the input number.
2. Add the digits of the number.
3. Replace the number with the sum.
4. Repeat steps 2–3 until a single digit is obtained.
5. If the final digit is 1, it is a Magic Number.

   ## 💻 Program


   #include <stdio.h>

/*
 A Magic Number is a number where the repeated sum of digits
 results in 1.
 Example: 19 -> 1+9=10 -> 1+0=1 (Magic Number)
*/

int main() {
    int num, sum;

    printf("Enter a number: ");
    scanf("%d", &num);

    /* Repeat until a single digit is obtained */
    while (num > 9) {
        sum = 0;
        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        num = sum;
    }

    /* Check Magic Number condition */
    if (num == 1)
        printf("It is a Magic Number.\n");
    else
        printf("It is not a Magic Number.\n");

    return 0;
}
