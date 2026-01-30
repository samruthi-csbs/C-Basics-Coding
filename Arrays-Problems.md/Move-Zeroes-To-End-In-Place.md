# Move Zeros to End (In-Place) — C

A C program that moves all `0`s to the end of the array **without using extra space**, while maintaining the order of non-zero elements.

## 📋 Description
- Reads array size and elements
- Rearranges the array in-place
- Prints the updated array

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n], pos = 0;
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    for (int i = 0; i < n; i++)
        if (arr[i] != 0)
            arr[pos++] = arr[i];

    while (pos < n)
        arr[pos++] = 0;

    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
