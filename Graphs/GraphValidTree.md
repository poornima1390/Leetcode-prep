DESCRIPTION (inspired by Lintcode.com)
You are given an integer n and a list of undirected edges where each entry in the list is a pair of integers representing an edge between nodes 0 and n - 1. You have to write a function to check whether these edges make up a valid tree.
There will be no duplicate edges in the edges list. (i.e. [0, 1] and [1, 0] will not appear together in the list).

Solution
Directed / Undirected - Undirected
Pattern - 
Valid tree is a fully connected undirected graph with no cycles
Two parts to the solution 1. no cycles 2. reach every node through dfs (fully connected)
