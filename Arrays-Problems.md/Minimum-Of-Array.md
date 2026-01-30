# Minimum Element in an Array (C)

A simple C program to find the **minimum element** in an array.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Finds and prints the smallest element  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int min = arr[0];
    for (int i = 1; i < n; i++) {
        if (arr[i] < min)
            min = arr[i];
    }

    printf("%d", min);
    return 0;
}
