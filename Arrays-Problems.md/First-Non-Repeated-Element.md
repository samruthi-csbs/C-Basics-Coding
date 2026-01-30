# 🌟 First Non-Repeated Element in an Array (C)

This program finds the **first non-repeated element** in an array of integers.  
Great for understanding arrays, loops, and counting occurrences 🧠💡

---

## 🔍 How it works

- Traverse the array
- For each element, count how many times it appears
- The first element with count = 1 is the answer ✅
- Simple approach: **O(n²)** time, **O(1)** extra space

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
    for(int i = 0; i < n; i++) {
        int count = 0;
        for(int j = 0; j < n; j++) {
            if(a[i] == a[j])
                count++;
        }
        if(count == 1) {
            printf("First non-repeated element is %d\n", a[i]);
            found = 1;
            break;
        }
    }

    if(!found)
        printf("No non-repeated elements found\n");

    return 0;
}
