# Reverse an Array Using Additional Array (C)

A C program to reverse an array using an extra array.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Reverses the array using an additional array  
- Prints the reversed array  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n], rev[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    // Reverse using extra array
    for (int i = 0; i < n; i++)
        rev[i] = arr[n - 1 - i];

    // Print reversed array
    for (int i = 0; i < n; i++)
        printf("%d ", rev[i]);

    return 0;
}


