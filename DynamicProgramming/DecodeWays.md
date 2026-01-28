Use a dp array to store the number of ways to decode for the characters till ith place. Two cases:
- If the digit is greater than 0, add the previous i - 1 value to i
- If the digit with the previous digit is in the range 10 - 26, then add the i - 2 value to i
