
# BFS vs DFS — Core Difference

| Traversal | Think                                         |
| --------- | --------------------------------------------- |
| **BFS**   | Level-by-level, shortest path, wave expansion |
| **DFS**   | Go deep, explore structure, backtracking      |

---

# 🔵 BFS PATTERNS (Level / Distance / Wave Problems)

BFS is almost always used when **distance, levels, or minimum steps** are involved.

---

## 1️⃣ Shortest Path (Unweighted Graph)

### Signal words:

* “minimum steps”
* “shortest path”
* “least moves”

### Examples:

* Word Ladder
* Shortest Path in Binary Matrix
* Rotting Oranges

### Pattern:

```java
queue → process level by level
distance = levels
```

---

## 2️⃣ Multi-Source BFS

### Signal:

* “multiple starting points”
* “spread simultaneously”

### Examples:

* Rotting Oranges
* Walls and Gates

### Pattern:

```java
add ALL sources to queue initially
then BFS
```

---

## 3️⃣ Level Order Traversal

### Signal:

* “level by level”
* “group nodes by level”

### Examples:

* Binary Tree Level Order Traversal

### Pattern:

```java
for each level:
    process size of queue
```

---

## 4️⃣ BFS on Grid (Flood + Distance)

### Signal:

* Matrix/grid
* shortest path / spread

### Examples:

* 01 Matrix
* Shortest Path in Grid

---

## 5️⃣ State-Space BFS

### Signal:

* Each node = “state”
* transformations / operations

### Examples:

* Word Ladder
* Open the Lock

---

## 6️⃣ Topological Sort (Kahn’s Algorithm)

### Signal:

* dependencies
* ordering
* DAG

### Pattern:

```java
indegree[]
queue → nodes with indegree 0
```

---

## 7️⃣ Bipartite Graph Check

### Signal:

* “2 groups”
* “no conflicts”

### Pattern:

```java
color nodes using BFS
if conflict → not bipartite
```

---

## 8️⃣ Shortest Path with Constraints

### Signal:

* k stops
* limited moves

### Example:

* Cheapest Flights Within K Stops

---

# 🟢 DFS PATTERNS (Structure / Exhaustive Search)

DFS is used when you need to **explore all possibilities or understand structure**.

---

## At its core, DFS follows this simple pattern:
```
dfs(node)
    if node is null
        return
    
    // process the current node
    
    dfs(node.left)
    dfs(node.right)
```
## For graphs, you also need to track visited nodes to avoid infinite loops:
```
dfs(node, visited)
    if node in visited
        return
    
    visited.add(node)
    
    for neighbor in node.neighbors
        dfs(neighbor, visited)
```
## 1️⃣ Counting Connected Components

### Signal:

* “number of islands”
* “groups”

### Examples:

* Number of Islands
* Number of Provinces

---

## 2️⃣ Flood Fill / Region Marking / Boundary DFS

### Signal:

* fill / replace / mark region

### Examples:

* Flood Fill
* Surrounded Regions

---

## 3️⃣ Backtracking (DFS + Undo)

### Signal:

* “all combinations”
* “generate all”
* “try all paths”

### Examples:

* Permutations
* Subsets
* Word Search

---

## 4️⃣ Cycle Detection

---

### Undirected

* parent tracking

### Directed

* recursion stack

---

## 5️⃣ Topological Sort (DFS version)

### Signal:

* ordering tasks

### Pattern:

```java
DFS + postorder stack
```

---

## 6️⃣ Tree Traversals

### Signal:

* preorder / inorder / postorder

---

## 7️⃣ Path Enumeration

### Signal:

* “all paths”
* “count paths”

### Examples:

* All Paths From Source to Target

---

## 8️⃣ Strongly Connected Components (Advanced)

### Algorithms:

* Kosaraju
* Tarjan

---

## 9️⃣ DFS on Grid

Same as BFS but:

* used when no shortest path needed
* just exploring regions

---

## 🔁 BFS vs DFS — When to Choose

| Situation                | Use  |
| ------------------------ | ---- |
| Shortest path            | BFS  |
| All paths / combinations | DFS  |
| Connected components     | Both |
| Cycle detection          | DFS  |
| Level order              | BFS  |
| Backtracking             | DFS  |
| Topological sort         | Both |

---

# Interview Mental Mapping (Fast Decision)

When problem appears:

---

### ❓ Is it shortest path?

→ BFS

---

### ❓ Is it exploring all possibilities?

→ DFS

---

### ❓ Is it grouping?

→ DFS/BFS

---

### ❓ Is it dependency ordering?

→ BFS (Kahn) or DFS

---

### ❓ Is it a grid?

→ BFS (distance) / DFS (explore)

---

#  Key Insight (This is what interviewers expect)

> BFS = **distance + levels**
> DFS = **structure + exploration**

---

#  Ultra-Condensed Cheat Sheet

### BFS triggers:

* shortest
* minimum
* level
* nearest
* spread

---

### DFS triggers:

* all
* count
* explore
* backtrack
* components

---
