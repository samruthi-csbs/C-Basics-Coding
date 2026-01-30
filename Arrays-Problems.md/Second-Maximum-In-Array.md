# Second Maximum Element in an Array (C)

A C program to find the **second largest element** in an array.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Finds the maximum and second maximum element  
- Prints the second largest element  

## 💻 Source Code
```c
#include <stdio.h>
#include <limits.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int max = INT_MIN, secondMax = INT_MIN;

    for (int i = 0; i < n; i++) {
        if (arr[i] > max) {
            secondMax = max;
            max = arr[i];
        } else if (arr[i] > secondMax && arr[i] != max) {
            secondMax = arr[i];
        }
    }

    if (secondMax == INT_MIN)
        printf("No second maximum");
    else
        printf("%d", secondMax);

    return 0;
}
