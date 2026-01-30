Given a 2D matrix, we should return the max area of square made up of only ones. Initially, create a dp array dp[r + 1][c + 1] to keep track of the side length of the largest square ending at matrix[i - 1][j - 1]. Keep a variable maxside to track the maxLength of the side of the max Area square. 
For the base case, fill the 1st row and column with the same number as matrix
The sub problem solution would be to find the min side length of the top, left and diagnol of the present cell and add 1 to it.
dp[i][j] = Math.min(top, Math.min(left, dia)) + 1
maxSide = Math.max(maxSide, dp[i][j])
do this only when matrix[i - 1][j - 1] is 1
return the area as maxSide * maxSide
