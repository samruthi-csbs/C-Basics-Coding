# 🫧 Bubble Sort in C

This C program sorts an array using **Bubble Sort** — one of the easiest sorting algorithms to understand 🧠💡

---

## 🔍 What is Bubble Sort?

- Repeatedly compares **adjacent elements**
- Swaps them if they are in the wrong order
- Larger elements “bubble up” to the end 🫧⬆️

---

## 🧠 How it Works

- Multiple passes through the array
- After each pass, the largest element is placed correctly
- Simple but not very fast for large data 😅

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
    for (int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (a[j] > a[j + 1]) {
                int temp = a[j];
                a[j] = a[j + 1];
                a[j + 1] = temp;
            }
        }
    }

    printf("Sorted array:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", a[i]);

    return 0;
}



⚙️ Complexity

⏱ Time Complexity: O(n²)

💾 Space Complexity: O(1)
