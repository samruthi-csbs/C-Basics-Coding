# LCM of Two Numbers in C

This program calculates the Least Common Multiple (LCM) of two integers using **GCD**.

## Logic:
1. Calculate GCD of two numbers using Euclid's algorithm.
2. Use the formula: LCM = |a * b| / GCD(a, b)

## Example:

Input: 12 18  
Output: LCM of 12 and 18 is 36


SAMPLE PROGRAM---
#include <stdio.h>

int main() {
    int a, b, lcm;

    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    // Make numbers positive
    int x = (a < 0) ? -a : a;
    int y = (b < 0) ? -b : b;

    // Start from max(x, y)
    lcm = (x > y) ? x : y;

    while (1) {
        if (lcm % x == 0 && lcm % y == 0) {
            break; // Found LCM
        }
        lcm++; // Increment to check next candidate
    }

    printf("LCM of %d and %d is %d\n", a, b, lcm);

    return 0;
}
