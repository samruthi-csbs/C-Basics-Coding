# Maximum Element in an Array (C)

A simple C program to find the **maximum element** in an array.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Finds and prints the largest element  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int max = arr[0];
    for (int i = 1; i < n; i++) {
        if (arr[i] > max)
            max = arr[i];
    }

    printf("%d", max);
    return 0;
}
