# Second Minimum in an Array (C)

This program finds the **second smallest distinct element** in an array using C.

## Example

Input:
5 1 2 1 3

Output:
Second minimum is 2

## Logic

- Store the smallest and second smallest values
- Traverse the array once
- Update values when a smaller element is found

## C Program

```c
#include <stdio.h>
#include <limits.h>

int main() {
    int arr[] = {5, 1, 2, 1, 3};
    int n = sizeof(arr) / sizeof(arr[0]);

    int min = INT_MAX;
    int second_min = INT_MAX;

    for (int i = 0; i < n; i++) {
        if (arr[i] < min) {
            second_min = min;
            min = arr[i];
        } else if (arr[i] > min && arr[i] < second_min) {
            second_min = arr[i];
        }
    }

    if (second_min == INT_MAX) {
        printf("Second minimum does not exist\n");
    } else {
        printf("Second minimum is %d\n", second_min);
    }

    return 0;
}
