# Rearrange Array: Even Numbers Before Odd Numbers (C)

A C program to rearrange an array so that all **even numbers appear before odd numbers**. The rearrangement is done **in-place** without preserving order.

## 📋 Description
- Reads the number of elements  
- Accepts array elements  
- Moves all even numbers to the front and odd numbers to the back  
- Prints the rearranged array  

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n];
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    int left = 0, right = n - 1;
    while (left < right) {
        while (arr[left] % 2 == 0 && left < right)
            left++;
        while (arr[right] % 2 != 0 && left < right)
            right--;
        if (left < right) {
            int temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;
            left++;
            right--;
        }
    }

    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
