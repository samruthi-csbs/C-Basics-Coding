# Sum of Array Elements in C

A simple and efficient C program that reads an array from user input and calculates the sum of its elements.

## 📋 Description
This program:
- Accepts the number of elements
- Reads integer values into an array
- Computes and prints the total sum

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }

    printf("%d", sum);
    return 0;
}
