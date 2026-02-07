In this problem, since the input is a 1D array and the number of unknown variables are just 1, we will create a 1D dp array where dp[i] gives the number of coins required to sum up to amount i with the given denominations. For the base case, fill the dp array with amount + 1 which is an impossible amount which helps us find the impossible combinations. The dp[0] = 0 will also be the other base. The solution of the sub problem would be dp[i] = Math.min(dp[i], dp[i - coin] + 1) while i - coin is greater than or equal to 0.
Return the last cell value while the value to not equal to amount + 1 if not return -1.
Time complexity: O(Amount∗Coins.Length)
Space Complexity: O(Amount)
