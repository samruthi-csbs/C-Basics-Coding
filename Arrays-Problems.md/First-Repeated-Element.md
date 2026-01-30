# 🔁 First Repeated Element in an Array (C)

This program finds the **first repeated element** in an array of integers.  
Perfect for learning arrays and nested loops 🧠💡

---

## 🔍 How it works

- Traverse the array
- For each element, check if it appears **again later**
- The first element that repeats is returned ✅
- Works in **O(n²)** time and **O(1)** space (simple approach)

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    int found = 0;
    for(int i = 0; i < n - 1; i++) {
        for(int j = i + 1; j < n; j++) {
            if(a[i] == a[j]) {
                printf("First repeated element is %d\n", a[i]);
                found = 1;
                break;
            }
        }
        if(found) break;
    }

    if(!found)
        printf("No repeated elements found\n");

    return 0;
}
