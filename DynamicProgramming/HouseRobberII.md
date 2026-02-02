A slight modification is required to bring this to the house robber I problem. Since the array is arranged circularly, split it into two linear arrays that is house 1 to n - 1 and house 2 to n. Create two dp arrays which computes the max profit in the both cases and finally return the max of the two arrays.

Time Complexity: O(N)
Space Complexity: O(N)
