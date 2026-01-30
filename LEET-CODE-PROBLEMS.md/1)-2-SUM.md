# ➕ Two Sum Problem (C)

## 📝 Problem Statement
**LeetCode #1: Two Sum**  
Given an array of integers `nums` and an integer `target`, return **indices of the two numbers** such that they add up to `target`.  
You may assume that each input would have exactly **one solution**, and you **may not use the same element twice**.  
You can return the answer in **any order**.

**Example 1:**  
Input: nums = [2,7,11,15], target = 9  
Output: [0,1]  

**Example 2:**  
Input: nums = [3,2,4], target = 6  
Output: [1,2]  

---

## 🔍 Explanation
- Traverse the array with **two nested loops**.  
- For each pair `(nums[i], nums[j])`, check if their **sum equals target**.  
- If yes → print the indices and exit.  
- Simple **O(n²)** brute-force approach ✅  
> 💡 For large arrays, a **hash table** can reduce time to O(n).

---

## 💻 C Code

```c
#include <stdio.h>

int main() {
    int n, target;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &nums[i]);

    printf("Enter target: ");
    scanf("%d", &target);

    // Brute-force search for the pair
    for(int i = 0; i < n-1; i++) {
        for(int j = i+1; j < n; j++) {
            if(nums[i] + nums[j] == target) {
                printf("Indices are [%d, %d]\n", i, j);
                return 0; // solution found
            }
        }
    }

    printf("No solution found\n");
    return 0;
}
