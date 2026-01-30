# Move All Negative Numbers to Beginning (In-Place) — C

A C program to move all negative numbers to the **beginning of the array** while keeping the order of non-negative numbers. The operation is done **in-place** without using extra space.

## 📋 Description
- Reads the number of elements
- Accepts array elements
- Moves negative numbers to the beginning
- Prints the rearranged array

## 💻 Source Code
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int arr[n], pos = 0;
    for (int i = 0; i < n; i++)
        scanf("%d", &arr[i]);

    // Move negatives to the front
    for (int i = 0; i < n; i++) {
        if (arr[i] < 0) {
            int temp = arr[i];
            // Shift elements to the right
            for (int j = i; j > pos; j--)
                arr[j] = arr[j-1];
            arr[pos++] = temp;
        }
    }

    // Print result
    for (int i = 0; i < n; i++)
        printf("%d ", arr[i]);

    return 0;
}
