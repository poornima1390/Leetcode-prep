Keep a dp array dp[r][c] to track the number of unique paths to the current cell. The base case would be to fill the first row and column with 1 since there is only one unique path to reach that cell. 
So to solve the sub problem, dp[i][j] = dp[i - 1][j] + dp[i][j - 1];
Return the last cell value.

Time Complexity: O(n*m)
Space Complexity: O(n*m)
