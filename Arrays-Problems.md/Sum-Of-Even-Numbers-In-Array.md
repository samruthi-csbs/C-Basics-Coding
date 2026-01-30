# Sum of Even Numbers in an Array (C)

A C program to calculate the sum of all even elements in an array.

## 📋 Description
The program:
- Reads the number of elements
- Accepts integer values into an array
- Adds only even numbers
- Prints the final sum

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        if (arr[i] % 2 == 0)
            sum += arr[i];
    }

    printf("%d", sum);
    return 0;
}
