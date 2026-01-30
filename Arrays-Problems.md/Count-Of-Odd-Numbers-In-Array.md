# Count of Odd Numbers in an Array (C)

A simple C program to count the number of odd elements in an array.

## 📋 Description
The program:
- Reads the number of elements
- Accepts integer values into an array
- Counts elements that are odd
- Prints the count

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n, count = 0;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        if (arr[i] % 2 != 0)
            count++;
    }

    printf("%d", count);
    return 0;
}
