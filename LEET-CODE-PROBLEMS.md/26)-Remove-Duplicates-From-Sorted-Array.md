# ❌ Remove Duplicates from Sorted Array (C)

## 📝 Problem Statement
**LeetCode #26: Remove Duplicates from Sorted Array**  

Given a **sorted integer array `nums`**, remove duplicates **in-place** such that each unique element appears **only once**.  
Return the **number of unique elements `k`**, with the first `k` elements of `nums` containing the unique numbers in sorted order.  
The remaining elements beyond index `k-1` can be ignored.

**Example 1:**  
Input: nums = [1,1,2]  
Output: 2, nums = [1,2,_]  

**Example 2:**  
Input: nums = [0,0,1,1,1,2,2,3,3,4]  
Output: 5, nums = [0,1,2,3,4,_,_,_,_,_]  

---

## 🔍 How It Works

- Since the array is **sorted**, duplicates are **consecutive**.  
- Use **two pointers**:
  - `i` → tracks the last unique element's position  
  - `j` → traverses the array  
- If `nums[j] != nums[i]`, increment `i` and **update `nums[i] = nums[j]`**  
- After traversal, `i+1` gives the number of unique elements `k`. ✅  
- **In-place solution** → O(1) extra space.

---

## 💻 C Code

```c
#include <stdio.h>

int removeDuplicates(int nums[], int n) {
    if(n == 0) return 0;

    int i = 0; // last unique element index
    for(int j = 1; j < n; j++) {
        if(nums[j] != nums[i]) {
            i++;
            nums[i] = nums[j];
        }
    }
    return i + 1; // number of unique elements
}

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d sorted elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &nums[i]);

    int k = removeDuplicates(nums, n);

    printf("Number of unique elements: %d\n", k);
    printf("Array after removing duplicates: ");
    for(int i = 0; i < k; i++)
        printf("%d ", nums[i]);
    printf("\n");

    return 0;
}
