# Check for Duplicates in an Array (C)

A C program to check whether an array contains duplicate elements.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Checks for duplicates using nested loops  
- Prints "Yes" if duplicates exist, otherwise "No"  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int found = 0;
    for (int i = 0; i < n-1; i++) {
        for (int j = i+1; j < n; j++) {
            if (arr[i] == arr[j]) {
                found = 1;
                break;
            }
        }
        if (found) break;
    }

    if (found)
        printf("Yes");
    else
        printf("No");

    return 0;
}
