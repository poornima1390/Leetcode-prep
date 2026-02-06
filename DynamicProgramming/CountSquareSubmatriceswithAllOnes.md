This problem is a continuation of the maximal square problem. Te concept is that, when we are trying to the find the maximal sqaure by finding the max side and storing it in the dp, we are also finding the possible squares in the matrix. So dp matrix represents the max side square that can be formed with matrix[i][j] being at the bottom right of the square. This is the exact solution of the maximal square. To find the count of the squares, we just have to find the sum of the dp matrix which will give the count of all the squares possible in the given matrix 2D array.

Time complexity: O(M∗N)
Space Complexity: O(M∗N)
