# Armstrong Number in C

This program checks whether a given number is an Armstrong number.  
Negative numbers are considered invalid for Armstrong check.

## Logic:
1. Count the number of digits in the number.
2. For each digit, raise it to the power of the number of digits.
3. Sum all these powers.
4. If the sum equals the original number → Armstrong, else → not Armstrong.

## Examples:

Input: 153  
Output: 153 is an Armstrong number.

Input: 123  
Output: 123 is not an Armstrong number.

SAMPLE CODE----



#include <stdio.h>
#include <math.h> // for pow()

int main() {
    int number, original, sum = 0, digit, numDigits = 0;
    
    printf("Enter a number: ");
    scanf("%d", &number);

    if (number < 0) {
        printf("Negative numbers cannot be Armstrong numbers.\n");
        return 0;
    }

    original = number;

    // Count number of digits
    int temp = number;
    while (temp != 0) {
        numDigits++;
        temp /= 10;
    }

    // Calculate sum of digits raised to the power of numDigits
    temp = number;
    while (temp != 0) {
        digit = temp % 10;
        sum += pow(digit, numDigits); // pow(base, exponent)
        temp /= 10;
    }

    if (sum == original) {
        printf("%d is an Armstrong number.\n", original);
    } else {
        printf("%d is not an Armstrong number.\n", original);
    }

    return 0;
}
