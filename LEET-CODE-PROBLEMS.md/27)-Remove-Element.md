# ❌ Remove Element (C)

## 📝 Problem Statement
**LeetCode #27: Remove Element**  

Given an integer array `nums` and an integer `val`, **remove all occurrences of `val` in-place**.  
Return the number of elements `k` in `nums` which are **not equal to `val`**.  

- The **first `k` elements** of `nums` should contain the elements not equal to `val`.  
- The **remaining elements** can be ignored.  
- The order of elements may be **changed**.  

**Example 1:**  
Input: nums = [3,2,2,3], val = 3  
Output: 2, nums = [2,2,_,_]  

**Example 2:**  
Input: nums = [0,1,2,2,3,0,4,2], val = 2  
Output: 5, nums = [0,1,4,0,3,_,_,_]  

---

## 🔍 How It Works

- Use **two pointers**:
  - `i` → tracks position to place next valid element  
  - `j` → traverses the array  
- If `nums[j] != val`, **move it to nums[i]** and increment `i`.  
- After traversal, `i` is the number of elements not equal to `val`. ✅  
- **In-place solution** → O(1) extra space.

> 💡 Simple, efficient, and widely used in **array manipulation problems**.

---

## 💻 C Code

```c
#include <stdio.h>

int removeElement(int nums[], int n, int val) {
    int i = 0; // next position for valid element
    for(int j = 0; j < n; j++) {
        if(nums[j] != val) {
            nums[i] = nums[j];
            i++;
        }
    }
    return i; // number of elements not equal to val
}

int main() {
    int n, val;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &nums[i]);

    printf("Enter value to remove: ");
    scanf("%d", &val);

    int k = removeElement(nums, n, val);

    printf("Number of elements not equal to %d: %d\n", val, k);
    printf("Array after removal: ");
    for(int i = 0; i < k; i++)
        printf("%d ", nums[i]);
    printf("\n");

    return 0;
}
