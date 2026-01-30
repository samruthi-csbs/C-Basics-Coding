# 💹 Best Time to Buy and Sell Stock (C)

## 📝 Problem Statement
**LeetCode #121: Best Time to Buy and Sell Stock**  

You are given an array `prices` where `prices[i]` is the price of a stock on the ith day.  

**Task:** Choose **one day to buy** and a **different future day to sell** the stock to **maximize profit**.  
Return the **maximum profit** you can achieve. If no profit is possible, return 0.  

**Example 1:**  
Input: prices = [7,1,5,3,6,4]  
Output: 5  
_Explanation: Buy on day 2 (price = 1), sell on day 5 (price = 6), profit = 6-1 = 5_

**Example 2:**  
Input: prices = [7,6,4,3,1]  
Output: 0  
_Explanation: No profit possible_

---

## 🔍 How It Works

- Track the **minimum price seen so far** as you iterate through the array.  
- At each day, calculate **profit = current price - min price so far**.  
- Keep track of the **maximum profit** found.  
- This ensures **buying before selling** automatically. ✅  

> 💡 Classic **single-pass array problem** — very efficient for interviews.

---

## 💻 C Code

```c
#include <stdio.h>

int maxProfit(int prices[], int n) {
    int minPrice = prices[0];
    int maxProfit = 0;

    for(int i = 1; i < n; i++) {
        if(prices[i] < minPrice)
            minPrice = prices[i];
        else if(prices[i] - minPrice > maxProfit)
            maxProfit = prices[i] - minPrice;
    }

    return maxProfit;
}

int main() {
    int n;
    printf("Enter number of days: ");
    scanf("%d", &n);

    int prices[n];
    printf("Enter prices for %d days:\n", n);
    for(int i = 0; i < n; i++)
        scanf("%d", &prices[i]);

    int profit = maxProfit(prices, n);
    printf("Maximum profit: %d\n", profit);

    return 0;
}
