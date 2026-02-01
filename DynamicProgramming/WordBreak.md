Since we have to find weather the string till ith position is can be segmented or not, we only need a 1D boolean dp array to keep track if or not the string can segmented till the ith position of the string. We require two loops i and j to extract the substring of the string, and if the dp[j] is true and the substring is present in the wordDict, then dp[i] is also true and break from the current itteration.
Return the last cell of the dp array.

Time Complexity: O(N^2)
Space Complexity: O(N)
