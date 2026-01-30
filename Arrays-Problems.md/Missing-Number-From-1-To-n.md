# 🔢 Find the Missing Number (1 to n)

This C program finds the **missing number** in a sequence from `1` to `n` using a **simple mathematical formula**.  
Efficient and beginner-friendly 💡✨

---

## 🔍 How it works

- Sum of numbers from 1 to n: `n*(n+1)/2`
- Sum all elements of the array
- Missing number = Total sum - Array sum 🧠

✅ Works in **O(n)** time and **O(1)** space  

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter n: ");
    scanf("%d", &n);

    int a[n-1];
    printf("Enter %d numbers (1 to %d with one missing):\n", n-1, n);
    for (int i = 0; i < n-1; i++)
        scanf("%d", &a[i]);

    int total = n*(n+1)/2;
    int sum = 0;

    for (int i = 0; i < n-1; i++)
        sum += a[i];

    int missing = total - sum;
    printf("Missing number is %d\n", missing);

    return 0;
}
