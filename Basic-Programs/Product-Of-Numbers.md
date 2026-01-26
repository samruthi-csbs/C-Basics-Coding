# Product of Digits in C
This program calculates the product of digits of a given integer.

## Logic:
1. Initialize product = 1
2. Extract each digit using % 10
3. Multiply product with the digit
4. Reduce number using / 10
5. Repeat until number becomes 0

## Example:
Input: 234
Output: 24


#include <stdio.h>

int main() {
    int number, product = 1, digit;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (number == 0) {
        product = 0; // edge case: 0 itself
    }

    while (number != 0) {
        digit = number % 10;   // extract last digit
        product *= digit;       // multiply with product
        number /= 10;           // remove last digit
    }

    printf("Product of digits = %d\n", product);
    return 0;
}
