# Check if an Array is Sorted in Descending Order (C)

A simple C program to check whether an array is sorted in **descending order**.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Checks if each element is greater than or equal to the next  
- Prints `Yes` if sorted in descending order, otherwise `No`  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int sorted = 1; // assume descending
    for (int i = 0; i < n-1; i++) {
        if (arr[i] < arr[i+1]) {
            sorted = 0;
            break;
        }
    }

    if (sorted)
        printf("Yes");
    else
        printf("No");

    return 0;
}
