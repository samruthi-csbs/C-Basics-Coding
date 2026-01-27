# Strong Number in C

## 📌 Description
A **Strong Number** is a number in which the **sum of the factorials of its digits**
is equal to the number itself.

### Example:
145  
= 1! + 4! + 5!  
= 1 + 24 + 120  
= **145** ✅ (Strong Number)

---

## 🧠 Algorithm
1. Read the input number.
2. Extract each digit using modulo (`%`).
3. Find factorial of each digit.
4. Add all factorial values.
5. Compare the sum with the original number.
6. Print the result.


#include <stdio.h>

/* Function to calculate factorial of a digit */
int factorial(int n) {
    int fact = 1;
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }
    return fact;
}

int main() {
    int num, temp, digit;
    int sum = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    temp = num;

    /* Calculate sum of factorials of digits */
    while (temp > 0) {
        digit = temp % 10;
        sum += factorial(digit);
        temp /= 10;
    }

    /* Check Strong Number condition */
    if (sum == num)
        printf("%d is a Strong Number.\n", num);
    else
        printf("%d is not a Strong Number.\n", num);

    return 0;
}
