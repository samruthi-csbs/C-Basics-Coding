# Reverse an Array In-Place (C)

A C program to reverse an array **without using any additional array**.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Reverses the array in-place using swapping  
- Prints the reversed array  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    // Reverse in-place
    for (int i = 0; i < n/2; i++) {
        int temp = arr[i];
        arr[i] = arr[n-1-i];
        arr[n-1-i] = temp;
    }

    // Print reversed array
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
