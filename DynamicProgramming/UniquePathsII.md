In continuation to the first path, for the base case, check if the previous cell is an obstacle, if not then add 1 or else add 0. To solve the sub problem, check if the matrix[i][j] is not an obstacle then perform the same solution as the first part which is dp[i][j] = dp[i - 1][j] + dp[i][j - 1].
Return the value of the last cell.
