# 🔀 Merge Two Sorted Arrays (C)

This C program merges **two sorted arrays** into **one sorted array**.  
A classic problem to understand arrays, pointers, and traversal 🧠💡

---

## 🔍 What does this program do?

- Takes size and elements of **two sorted arrays**
- Merges them into a **single sorted array**
- Does **not** sort again (efficient merge logic ⚡)

---

## 🧠 Core Idea

- Use three indices:
  - one for first array
  - one for second array
  - one for merged array
- Compare elements and insert the smaller one
- Copy remaining elements at the end

Simple and efficient 👍

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n1, n2;

    printf("Enter size of first array: ");
    scanf("%d", &n1);
    int a[n1];

    printf("Enter %d sorted elements:\n", n1);
    for (int i = 0; i < n1; i++)
        scanf("%d", &a[i]);

    printf("Enter size of second array: ");
    scanf("%d", &n2);
    int b[n2];

    printf("Enter %d sorted elements:\n", n2);
    for (int i = 0; i < n2; i++)
        scanf("%d", &b[i]);

    int c[n1 + n2];
    int i = 0, j = 0, k = 0;

    while (i < n1 && j < n2) {
        if (a[i] < b[j])
            c[k++] = a[i++];
        else
            c[k++] = b[j++];
    }

    while (i < n1)
        c[k++] = a[i++];

    while (j < n2)
        c[k++] = b[j++];

    printf("Merged array:\n");
    for (i = 0; i < n1 + n2; i++)
        printf("%d ", c[i]);

    return 0;
}
