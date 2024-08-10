---
title: "Best Time to Buy and Sell Stock"
weight: -20
---

### Best Time to Buy and Sell Stock :green_book:

##### Problem

You are given an array `prices` where `prices[i]` is the price of a given stock on the `ith` day. You want to maximize your profit by choosing a **single day** to buy one stock and choosing a **different day in the future** to sell that stock. Return *the maximum profit you can achieve from this transaction*. If you cannot achieve any profit, return `0`.

##### Solution

We want to keep track of the minimum price so far as we iterate through the prices. This will be the "buy" point. If the current price is the minimum price, then we should forget about selling (that's how you lose money). Now if it's not the minimum, we can determine a profit margin by comparing the current price with the minimum. If the profit margin is higher than previous profit margins than we keep this one as our "sell" point for most money. 

Time Complexity: O(n)

Space Complexity: O(1)

```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        max_profit = 0
        min_price = float("inf")
        for price in prices:
            if price < min_price:
                min_price = price
            elif price - min_price > max_profit:
                max_profit = price - min_price
        return max_profit	
```