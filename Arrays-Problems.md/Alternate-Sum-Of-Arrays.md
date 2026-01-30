# Alternate Sum of Array Elements (C)

A C program to calculate the alternate sum of elements in an array  
(add elements at even indices and subtract elements at odd indices).

## 📋 Description
The program:
- Reads the number of elements
- Accepts array values from user input
- Computes the alternate sum
- Prints the result

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n, sum = 0;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    for (int i = 0; i < n; i++) {
        if (i % 2 == 0)
            sum += arr[i];
        else
            sum -= arr[i];
    }

    printf("%d", sum);
    return 0;
}
