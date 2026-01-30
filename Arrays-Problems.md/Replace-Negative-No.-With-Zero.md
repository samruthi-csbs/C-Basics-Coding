# Replace Negative Numbers with Zero in an Array (C)

A simple C program to replace all negative numbers in an array with `0`.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Replaces every negative number with `0`  
- Prints the updated array  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        if (arr[i] < 0)
            arr[i] = 0;
    }

    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
