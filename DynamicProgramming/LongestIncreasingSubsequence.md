Given a 1D matrix, create a 1D dp array to track the length of the longest increasing subsequence. The base case would dp[0] = 1 since the length of one number is 1. To solve the sub problem, keep two arrays: one starting from 1 to length of array and other starting from 0 to i. At each iteration if nums[i] > nums[j] then increament dp[i] = dp[j] + 1
Return the max number in the array by streaming : Arrays.stream(dp).max().orElse(0)

Time complexity: O(N^2)
Space complexity: O(N)
