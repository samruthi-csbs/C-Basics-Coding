# Check if All Elements in an Array are Distinct (C)

A C program to check whether all elements in an array are **distinct** (no duplicates).

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Checks for duplicate values using nested loops  
- Prints `Yes` if all elements are distinct, otherwise `No`  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int distinct = 1; // assume all elements are distinct
    for (int i = 0; i < n-1; i++) {
        for (int j = i+1; j < n; j++) {
            if (arr[i] == arr[j]) {
                distinct = 0;
                break;
            }
        }
        if (!distinct) break;
    }

    if (distinct)
        printf("Yes");
    else
        printf("No");

    return 0;
}
