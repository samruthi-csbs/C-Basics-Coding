# GCD of Two Numbers in C

This program calculates the Greatest Common Divisor (GCD) of two integers using **Euclid's Algorithm**.

## Logic:
1. Take two numbers a and b.
2. While b != 0:
   - r = a % b
   - a = b
   - b = r
3. When b becomes 0, a is the GCD.

## Example:

Input: 48 18  
Output: GCD of 48 and 18 is 6


## SAMPLE CODE:

#include <stdio.h>

int main() {
    int a, b, temp;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    int x = a, y = b;

    // Make numbers positive
    if (x < 0) x = -x;
    if (y < 0) y = -y;

    // Euclid's algorithm
    while (y != 0) {
        temp = y;
        y = x % y;
        x = temp;
    }

    printf("GCD of %d and %d is %d\n", a, b, x);

    return 0;
}
