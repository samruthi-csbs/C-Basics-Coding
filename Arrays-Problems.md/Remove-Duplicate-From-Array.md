# ❌ Remove Duplicates from an Array (C)

This C program removes **duplicate elements** from an array and keeps only **unique elements**.  
Great exercise for arrays and loops 🧠💡

---

## 🔍 How it works

- Traverse the array
- For each element, check if it has appeared before
- Copy only **unique elements** to a new array  
- Simple **O(n²)** approach ✅

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n], unique[n];
    int k = 0; // count of unique elements

    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    for(int i = 0; i < n; i++) {
        int isDuplicate = 0;
        for(int j = 0; j < k; j++) {
            if(a[i] == unique[j]) {
                isDuplicate = 1;
                break;
            }
        }
        if(!isDuplicate)
            unique[k++] = a[i];
    }

    printf("Array after removing duplicates:\n");
    for(int i = 0; i < k; i++)
        printf("%d ", unique[i]);

    return 0;
}
