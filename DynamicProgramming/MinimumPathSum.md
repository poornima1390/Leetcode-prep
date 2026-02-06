This problem asks us to find the path with min sum in a 2D matrix. Create a 2D array and for the base case fill the first row and first column with the contiguous sum of the path. To solve the sub problem, dp[i][j] will the min of dp[i - 1][j] + nums[i][j] or dp[i][j - 1] + nums[i][j]. This will give the min sum of a path. Return the answer with dp[m - 1][n - 1].

Time Complexity: O(M*N)
Space Complexity: O(M*N)
