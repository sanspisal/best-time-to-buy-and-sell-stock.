# Best Time to Buy and Sell Stock

This repository contains a C++ implementation of the "Best Time to Buy and Sell Stock" problem.

## Problem Description

You are given an array `prices` where `prices[i]` is the price of a given stock on the `i`th day. You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock. Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return `0`.

## Solution

The solution uses a single pass approach to find the maximum profit. It maintains three variables: 
- `buy_price` to keep track of the minimum price encountered so far
- `current_profit` to calculate the profit for the current day
- `max_profit` to store the maximum profit that can be achieved.

### Code Explanation

- **Initialize `buy_price`** to the first price in the array.
- **Initialize `current_profit`** to `0`.
- **Initialize `max_profit`** to `0`.
- **Iterate through the prices** starting from the second element:
  - If the current price is less than `buy_price`, update `buy_price`.
  - Otherwise, calculate `current_profit` as the difference between the current price and `buy_price`.
  - Update `max_profit` to be the maximum of `current_profit` and the previous `max_profit`.

### Example

Given the prices `[7, 1, 5, 3, 6, 4]`, the maximum profit is `5`, which is achieved by buying at `1` and selling at `6`.

#Time complexity = O(n)
#Space complextiy= O(1).
