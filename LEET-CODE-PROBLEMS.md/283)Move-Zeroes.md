# 0️⃣ Move Zeroes (C)

## 📝 Problem Statement
**LeetCode #283: Move Zeroes**  

Given an integer array `nums`, **move all 0's to the end** while maintaining the **relative order of non-zero elements**.  
**Do it in-place** without making a copy of the array.

**Example 1:**  
Input: nums = [0,1,0,3,12]  
Output: [1,3,12,0,0]  

**Example 2:**  
Input: nums = [0]  
Output: [0]  

---

## 🔍 How It Works

- Use **two pointers**:  
  - `i` → tracks the position to place the next non-zero element  
  - `j` → iterates through the array  
- If `nums[j] != 0`, assign `nums[i] = nums[j]` and increment `i`  
- After placing all non-zero elements, **fill remaining positions with 0** ✅  
- **In-place solution**, O(n) time, O(1) space  

> 💡 Efficient way to **reorder arrays while preserving relative order**.

---

## 💻 C Code

```c
#include <stdio.h>

void moveZeroes(int nums[], int n) {
    int i = 0; // position for next non-zero
    for(int j = 0; j < n; j++) {
        if(nums[j] != 0) {
            nums[i] = nums[j];
            i++;
        }
    }
    // fill remaining positions with 0
    for(int k = i; k < n; k++)
        nums[k] = 0;
}

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &nums[i]);

    moveZeroes(nums, n);

    printf("Array after moving zeroes: ");
    for(int i = 0; i < n; i++)
        printf("%d ", nums[i]);
    printf("\n");

    return 0;
}
