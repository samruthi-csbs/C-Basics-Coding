# Palindrome Number in C

This program checks whether a given number is a palindrome or not.  
Negative numbers are considered not palindromes.

## Logic:
1. Store the original number.
2. Reverse the number using `% 10` and `/ 10`.
3. Compare reversed number with original.
4. If equal → palindrome, else → not palindrome.

## Examples:

Input: 121  
Output: 121 is a palindrome.

Input: 123  
Output: 123 is not a palindrome.

Input: -121  
Output: Negative numbers are not palindromes.



SAMPLE PROGRAME---
#include <stdio.h>

int main() {
    int number, original, reversed = 0, digit;

    printf("Enter a number: ");
    scanf("%d", &number);

    // Negative numbers are not palindromes
    if (number < 0) {
        printf("Negative numbers are not palindromes.\n");
        return 0;
    }

    original = number; // store original number

    while (number != 0) {
        digit = number % 10;           // get last digit
        reversed = reversed * 10 + digit; // build reversed number
        number /= 10;                  // remove last digit
    }

    if (reversed == original) {
        printf("%d is a palindrome.\n", original);
    } else {
        printf("%d is not a palindrome.\n", original);
    }

    return 0;
}
