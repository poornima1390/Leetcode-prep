Since there are two variables given, we are supposed to compare and find the common characters so having a 2D array is helpful. dp[i][j] represents the length of the longest increasing subsequence until that point in both strings. To solve the subproblem, if the character of text1 and text2 is same, then dp[i][j] = dp[i - 1][j - 1] + 1 else dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]). Return the value of the last cell.
Time complexity: O(m * n)
Space Complexity: O(m * n)
