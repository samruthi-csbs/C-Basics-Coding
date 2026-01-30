# ❓ Missing Number (C)

## 📝 Problem Statement
**LeetCode #268: Missing Number**  

Given an array `nums` containing **n distinct numbers** in the range `[0, n]`, return the **only number in the range that is missing** from the array.

**Example 1:**  
Input: nums = [3,0,1]  
Output: 2  
_Explanation: Range [0,3], missing number is 2_

**Example 2:**  
Input: nums = [0,1]  
Output: 2  
_Explanation: Range [0,2], missing number is 2_

**Example 3:**  
Input: nums = [9,6,4,2,3,5,7,0,1]  
Output: 8  
_Explanation: Range [0,9], missing number is 8_

---

## 🔍 How It Works

**Approach 1: Sum Formula**  
- Sum of numbers from `0` to `n` is `n*(n+1)/2`  
- Subtract the sum of elements in the array → result is **missing number**  

**Approach 2: XOR Trick**  
- XOR all numbers from `0` to `n` and XOR all elements in `nums`  
- Duplicates cancel out → result is **missing number** ✅  

> 💡 Both approaches are **O(n) time** and **O(1) space**.

---

## 💻 C Code (Sum Formula)

```c
#include <stdio.h>

int missingNumber(int nums[], int n) {
    int sum = n*(n+1)/2;
    int arraySum = 0;
    for(int i = 0; i < n; i++)
        arraySum += nums[i];
    return sum - arraySum;
}

int main() {
    int n;
    printf("Enter number of elements: ");
    scanf("%d", &n);

    int nums[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &nums[i]);

    int missing = missingNumber(nums, n);
    printf("The missing number is: %d\n", missing);

    return 0;
}
