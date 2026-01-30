# 🔍 Linear Search in an Array (C)

This program searches for an element in an array using **linear search** — the simplest search algorithm.  
Great for beginners to understand arrays and loops 🧠💡

---

## 🔍 How it works

- Traverse the array **from start to end**
- Compare each element with the target
- If found → return the index
- If not found → report element not present ✅

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n, key, found = 0;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    printf("Enter element to search: ");
    scanf("%d", &key);

    for(int i = 0; i < n; i++) {
        if(a[i] == key) {
            printf("Element found at index %d\n", i);
            found = 1;
            break;
        }
    }

    if(!found)
        printf("Element not found\n");

    return 0;
}
