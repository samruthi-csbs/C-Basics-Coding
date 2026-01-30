# 🇳🇱 Dutch National Flag Algorithm in C

This program sorts an array containing only **0s, 1s, and 2s** using the **Dutch National Flag Algorithm**.  
Efficient, simple, and runs in **O(n) time** 🟢⚪🔴

---

## 🔍 How it works

- Maintain **three pointers**: `low`, `mid`, `high`
- Rules:
  - `0` → move to the **beginning**
  - `1` → keep in the **middle**
  - `2` → move to the **end**
- Single traversal, no extra space 💡

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int a[n];
    printf("Enter %d elements (0,1,2 only):\n", n);
    for (int i = 0; i < n; i++)
        scanf("%d", &a[i]);

    int low = 0, mid = 0, high = n - 1;

    while (mid <= high) {
        if (a[mid] == 0) {
            int temp = a[low];
            a[low] = a[mid];
            a[mid] = temp;
            low++; mid++;
        } else if (a[mid] == 1) {
            mid++;
        } else { // a[mid] == 2
            int temp = a[mid];
            a[mid] = a[high];
            a[high] = temp;
            high--;
        }
    }

    printf("Sorted array:\n");
    for (int i = 0; i < n; i++)
        printf("%d ", a[i]);

    return 0;
}
⚙️ Complexity
⏱ Time Complexity: O(n)

💾 Space Complexity: O(1)

