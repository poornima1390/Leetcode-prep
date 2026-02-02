Kadane's algorithm:
currSum = Math.max(nums[i], nums[i] + currSum)
maxSum = Math.max(currSum, maxSum)
Use when subarray is contiguous and there are negative numbers and you have to find max sum or min sum.

Time Complexity: O(N)
Space Complexity: O(1)
