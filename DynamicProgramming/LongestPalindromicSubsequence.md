Approach 1:
Converting the problem to LCS and following the same process to solve the subproblem. Firstly create 2D dp array ad initialize the first row and first column with zeros. The row represents normal string and the column represents the reversed version of the string. To solve the sub problem, if the characters are same then dp[i][j] = dp[i - 1][j - 1] + 1 if not then dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]). Return the last cell value of the array.
Time complexity: O(N^2)
Space Complexity: O(N^2)
