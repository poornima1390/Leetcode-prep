What am I optimizing / counting / deciding? minimizing the number of operations 
What is the DP state? 2D dp where the dp represents the min number of operations required 
What is the transition? if the characters are same: dp[i][j] = dp[i - 1][j - 1] if not: dp[i][j] = 1 + Math.min(dp[i - 1][j], Math.min(dp[i][j - 1], dp[i - 1][j - 1]))
What is the base case? dp[0][0] = 0, dp[i][0] = i, dp[0][i] = i 
Does loop order matter here? no, row represent word2 and col represents word1
