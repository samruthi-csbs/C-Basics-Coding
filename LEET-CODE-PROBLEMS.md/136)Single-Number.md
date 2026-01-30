# 🔢 Single Number (C)

## 📝 Problem Statement
**LeetCode #136: Single Number**  

Given a non-empty array of integers `nums`, every element appears **twice except for one**.  
Find the element that appears **only once**.  

**Requirements:**  
- Linear runtime complexity **O(n)**  
- Constant extra space **O(1)**  

**Example 1:**  
Input: nums = [2,2,1]  
Output: 1  

**Example 2:**  
Input: nums = [4,1,2,1,2]  
Output: 4  

**Example 3:**  
Input: nums = [1]  
Output: 1  

---

## 🔍 How It Works

- Use the **XOR operation (^)**:  
  - `a ^ a = 0` → duplicates cancel out  
  - `0 ^ b = b` → single element remains  
- Traverse the array and **XOR all elements**.  
- The result is the **single number**. ✅  

> 💡 Very efficient, uses **bit manipulation**, a classic interview technique.

---

## 💻 C Code

```c
#include <stdio.h>

int singleNumber(int nums[], int n) {
    int result = 0;
    for(int i = 0; i < n; i++)
        result ^= nums[i]; // XOR all elements
    return result;
}

int main()
