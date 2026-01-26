# Reverse Number in C

This program reverses a given integer number. It works for both positive and negative numbers.

## Logic:
1. Take the absolute value of the number.
2. Extract last digit using `% 10`.
3. Add digit to reversed using `reversed = reversed * 10 + digit`.
4. Remove last digit using `/ 10`.
5. Repeat until number becomes 0.
6. Reapply sign if original number was negative.

## Example:
Input: -1234
Output: -4321

SAMPLE CODE-----


#include <stdio.h>

int main() {
    int number, reversed = 0, digit, sign = 1;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (number < 0) {
        sign = -1;
        number = -number; // work with positive
    }

    while (number != 0) {
        digit = number % 10;           // get last digit
        reversed = reversed * 10 + digit; // add to reversed
        number /= 10;                  // remove last digit
    }

    reversed *= sign; // reapply sign if negative
    printf("Reversed number = %d\n", reversed);

    return 0;
}
