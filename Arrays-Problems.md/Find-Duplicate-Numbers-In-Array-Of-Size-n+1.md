# 🔁 Find Duplicate in Array (C)

This C program finds the **duplicate number** in an array of size **n+1** containing numbers from **1 to n**.  
Classic problem for arrays and logical thinking 🧠💡

---

## 🔍 Problem

- Array size = n+1  
- Numbers = 1 to n  
- At least **one number is repeated**  
- Find **any duplicate** efficiently ✅

---

## 💻 C Code (Simple O(n²) Approach)

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter n (array size will be n+1): ");
    scanf("%d", &n);

    int a[n+1];
    printf("Enter %d numbers (1 to %d):\n", n+1, n);
    for(int i = 0; i <= n; i++)
        scanf("%d", &a[i]);

    int found = 0;
    for(int i = 0; i <= n; i++) {
        for(int j = i+1; j <= n; j++) {
            if(a[i] == a[j]) {
                printf("Duplicate number is %d\n", a[i]);
                found = 1;
                break;
            }
        }
        if(found) break;
    }

    if(!found)
        printf("No duplicates found\n");

    return 0;
}
