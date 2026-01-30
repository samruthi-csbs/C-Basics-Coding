# ➕ Plus One (C)

## 📝 Problem Statement
**LeetCode #66: Plus One**  

You are given a large integer represented as an integer array `digits`, where each `digits[i]` is the ith digit of the integer.  
The digits are ordered from **most significant to least significant** (left-to-right), and the integer **does not contain leading zeros**.  

**Task:** Increment the large integer by **one** and return the resulting array of digits.

**Example 1:**  
Input: digits = [1,2,3]  
Output: [1,2,4]  
_Explanation: 123 + 1 = 124_

**Example 2:**  
Input: digits = [4,3,2,1]  
Output: [4,3,2,2]  
_Explanation: 4321 + 1 = 4322_

**Example 3:**  
Input: digits = [9]  
Output: [1,0]  
_Explanation: 9 + 1 = 10_

---

## 🔍 How It Works

- Start from the **least significant digit** (end of array)  
- **Add 1** to the last digit  
- If it becomes 10 → set to 0 and **carry 1** to the next left digit  
- Repeat for all digits  
- If carry is still 1 after the most significant digit → **insert 1 at the beginning**  
- Works for **any length of array** ✅

> 💡 This is a classic **array manipulation and carry propagation** problem.

---

## 💻 C Code

```c
#include <stdio.h>
#include <stdlib.h>

void plusOne(int digits[], int n) {
    int carry = 1; // initial +1
    for(int i = n-1; i >= 0; i--) {
        int sum = digits[i] + carry;
        digits[i] = sum % 10;
        carry = sum / 10;
    }

    if(carry) { // need extra space for new most significant digit
        printf("Result: 1 ");
        for(int i = 0; i < n; i++)
            printf("%d ", digits[i]);
        printf("\n");
    } else {
        printf("Result: ");
        for(int i = 0; i < n; i++)
            printf("%d ", digits[i]);
        printf("\n");
    }
}

int main() {
    int n;
    printf("Enter number of digits: ");
    scanf("%d", &n);

    int digits[n];
    printf("Enter %d digits (most significant to least significant):\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &digits[i]);

    plusOne(digits, n);

    return 0;
}
