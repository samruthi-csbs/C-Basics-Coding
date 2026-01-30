# 🔎 Binary Search in an Array (C)

This program searches for an element in a **sorted array** using **Binary Search** — an efficient search algorithm 🧠💡

---

## 🔍 How it works

- Works **only on sorted arrays**
- Repeatedly divides the search range in half:
  - Check middle element
  - If target < middle → search left
  - If target > middle → search right
- Stops when element is found or range is empty ✅

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n, key;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];
    printf("Enter %d elements in sorted order:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    printf("Enter element to search: ");
    scanf("%d", &key);

    int low = 0, high = n-1, found = 0;

    while(low <= high) {
        int mid = low + (high - low)/2;

        if(a[mid] == key) {
            printf("Element found at index %d\n", mid);
            found = 1;
            break;
        } else if(a[mid] < key) {
            low = mid + 1;
        } else {
            high = mid - 1;
        }
    }

    if(!found)
        printf("Element not found\n");

    return 0;
}
