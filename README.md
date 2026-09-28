# LeetCode 312 - Burst Balloons

## Problem Statement

You are given an array of balloons, where each balloon has a number written on it.

When you burst a balloon, you gain coins equal to the product of the numbers of the balloon itself and its two adjacent balloons.

Return the maximum number of coins you can collect by bursting the balloons in the best possible order.

## Example 1

### Input

```text
nums = [3,1,5,8]
```

### Output

```text
167
```

## Example 2

### Input

```text
nums = [1,5]
```

### Output

```text
10
```

## Approach

Use **Dynamic Programming** with interval partitioning.

Instead of deciding which balloon to burst first, consider which balloon is burst **last** within a given range.

When a balloon is burst last, its left and right neighbors are known, making the calculation easier.

## Algorithm

1. Add `1` to both ends of the array.
2. Create a DP table where `dp[left][right]` stores the maximum coins obtainable between `left` and `right`.
3. Consider intervals of increasing length.
4. For each interval, try every balloon as the last balloon to burst.
5. Calculate the coins gained from bursting that balloon last.
6. Add the best results from the left and right subintervals.
7. Store the maximum value in the DP table.
8. Return the maximum value for the complete interval.

## Time Complexity

`O(n³)`

## Space Complexity

`O(n²)`

## Key Concepts

* Dynamic Programming
* Interval DP
* Arrays
* Recursion Optimization
* Subproblems
* Matrix-Style DP

## Language

Python

## LeetCode Details

* **Problem:** 312
* **Title:** Burst Balloons
* **Difficulty:** Hard

## Author

**T. Nandhini Reddy**

GitHub: `242t605119-dotcom`
