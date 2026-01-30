# 🏆 Kth Maximum Element in an Array (C)

This C program finds the **kth maximum element** from an array of **distinct integers**.  
Perfect for learning arrays, loops, and basic sorting 💡

---

## 🔍 What does it do?

- Takes array size and elements from the user
- Takes `k` as input
- Sorts the array in **descending order**
- Prints the **kth maximum element**

✅ Assumes all elements are **distinct**

---

## 🧠 Idea Behind the Code

- Sort the array from largest → smallest
- The element at index `k-1` is the kth maximum

Simple and easy to understand 👍

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n, k;

    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];

    printf("Enter %d distinct elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    printf("Enter k: ");
    scanf("%d", &k);

    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (a[i] < a[j]) {
                int temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
    }

    printf("Kth maximum element is %d\n", a[k - 1]);
    return 0;
}
