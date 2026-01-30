# Count Number of Zeros in an Array (C)

A C program to count how many zero values are present in an array.

## 📋 Description
The program:
- Reads the number of elements
- Accepts integer values into an array
- Counts elements equal to zero
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
        if (arr[i] == 0)
            count++;
    }

    printf("%d", count);
    return 0;
}
