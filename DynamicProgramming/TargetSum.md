The key step to solve this problem is to convert the problem to a subset sum problem. To do this first calculate totalSum of the nums array, then apply the following formula to find P = (totalSum + target) / 2. The target now becomes P. Creatre a 1D dp array of size new target + 1. The base case of the problem is, dp[0] = 1. The first loop will be of the nums array and the second array will be of the dp array but in the reverse order, this ensures the count is not repeated. The solution of the dp is dp[i] += dp[num - i].
Return the last cell value.
Time complexity: O(n *m)
Space Complexity: O(N)
