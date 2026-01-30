Input: nums = [1,2,3,1]
Output: 4 (maximum profit by robbing non adjacent houses)

Approach: since the problem can be solved by solving the sub problems, the right approach would be to use dynamic programming. By storing the max profit till ith house will help calculate the final profit at the last house.
It's important to verify the right base case for this problem.

Time Complexity: O(N)
Space Complexity: O(N)
