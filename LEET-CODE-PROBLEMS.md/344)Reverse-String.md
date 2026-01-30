# 🔄 Reverse String (C)

## 📝 Problem Statement
**LeetCode #344: Reverse String**  

Write a function that **reverses a string**. The input string is given as an array of characters `s`.  

**Requirements:**  
- Modify the array **in-place**  
- Use **O(1) extra memory**

**Example 1:**  
Input: s = ["h","e","l","l","o"]  
Output: ["o","l","l","e","h"]  

**Example 2:**  
Input: s = ["H","a","n","n","a","h"]  
Output: ["h","a","n","n","a","H"]  

---

## 🔍 How It Works

- Use **two-pointer technique**:  
  - `left` points to the start of the array  
  - `right` points to the end of the array  
- Swap `s[left]` and `s[right]`  
- Move `left++` and `right--` until `left >= right`  
- **In-place solution**, O(n) time, O(1) space ✅  

> 💡 Elegant and efficient for **array/string reversal problems**.

---

## 💻 C Code

```c
#include <stdio.h>

void reverseString(char s[], int n) {
    int left = 0, right = n - 1;
    while(left < right) {
        char temp = s[left];
        s[left] = s[right];
        s[right] = temp;
        left++;
        right--;
    }
}

int main() {
    int n;
    printf("Enter number of characters: ");
    scanf("%d", &n);

    char s[n+1]; // +1 for null terminator if needed
    printf("Enter the characters (no spaces): ");
    for(int i = 0; i < n; i++)
        scanf(" %c", &s[i]);

    reverseString(s, n);

    printf("Reversed string: ");
    for(int i = 0; i < n; i++)
        printf("%c", s[i]);
    printf("\n");

    return 0;
}
