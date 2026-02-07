This is an unbounded knapsack counting problem. I define dp[x] as the number of ways to form amount x. Base case is dp[0] = 1.
To avoid counting permutations, I iterate coins first, then amounts.
For each coin, I add ways from dp[x - coin], so dp[i] = dp[i] + dp[i - coin]
Return the last cell value.
Time complexity: O(amount * coins.length)
Space complexity: O(amount)
