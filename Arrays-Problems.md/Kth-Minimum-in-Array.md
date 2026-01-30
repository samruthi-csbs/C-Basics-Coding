# 🥇 Kth Minimum Element in an Array (C)

This C program finds the **kth minimum element** from an array of **distinct integers**.  
A great problem to practice arrays, loops, and sorting 🧠💻

---

## 🔍 What does this program do?

- Takes array size from the user
- Reads distinct elements
- Takes `k` as input
- Sorts the array in **ascending order**
- Prints the **kth minimum element**

✅ Assumes all elements are **distinct**

---

## 🧠 Simple Logic

- Sort the array from smallest → largest
- The element at index `k-1` is the kth minimum 🎯

Easy and beginner-friendly ✨

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
            if (a[i] > a[j]) {
                int temp = a[i];
                a[i] = a[j];
                a[j] = temp;
            }
        }
    }

    printf("Kth minimum element is %d\n", a[k - 1]);
    return 0;
}
