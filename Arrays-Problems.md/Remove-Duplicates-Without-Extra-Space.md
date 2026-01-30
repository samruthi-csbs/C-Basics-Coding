# ❌ Remove Duplicates In-Place (C)

This program removes **duplicate elements from an array without using extra space**.  
It keeps only **unique elements in the original array**. 🧠✨

---

## 🔍 How it works

- **Sort the array first** (so duplicates are consecutive)  
- Traverse the array, and move only **unique elements forward**  
- Works in-place → no extra array needed ✅

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

    // Step 1: Sort array (simple bubble sort)
    for(int i = 0; i < n-1; i++) {
        for(int j = 0; j < n-i-1; j++) {
            if(a[j] > a[j+1]) {
                int temp = a[j];
                a[j] = a[j+1];
                a[j+1] = temp;
            }
        }
    }

    // Step 2: Remove duplicates in-place
    int k = 0; // index of last unique element
    for(int i = 1; i < n; i++) {
        if(a[i] != a[k]) {
            k++;
            a[k] = a[i];
        }
    }

    printf("Array after removing duplicates:\n");
    for(int i = 0; i <= k; i++)
        printf("%d ", a[i]);

    return 0;
}
