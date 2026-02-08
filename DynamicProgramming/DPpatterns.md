The 10-Second DP Checklist (Memorize This)

Before coding, mentally answer:

What am I optimizing / counting / deciding?

What is the DP state?

What is the transition?

What is the base case?

Does loop order matter here?

# 🧠 Dynamic Programming Pattern Table (Interview Mastery)

## 1️⃣ Linear DP (1D, prefix-based)

### 🔹 Pattern

Each state depends on a few **previous indices**.

### 🔹 State

```
dp[i] = answer up to index i
```

### 🔹 Transition

Usually `i-1`, `i-2`, etc.

### 🔹 Problems

* House Robber
* Climbing Stairs
* Fibonacci
* Decode Ways
* Max Subarray (Kadane)

### 🔹 Template

```java
dp[0] = base;
dp[1] = base;

for (int i = 2; i < n; i++) {
    dp[i] = combine(dp[i-1], dp[i-2]);
}
```

### 🔹 Interview Tip

If index `i` only depends on **earlier indices**, think **1D DP**.

---

## 2️⃣ Two-State DP (Take / Skip)

### 🔹 Pattern

At each step, you **choose or skip**.

### 🔹 State

```
dp[i][0/1] → skip / take
```

### 🔹 Problems

* Best Time to Buy & Sell Stock
* House Robber variants
* Stock with cooldown / fee

### 🔹 Example

```java
dp[i][0] = max(dp[i-1][0], dp[i-1][1] + price);
dp[i][1] = max(dp[i-1][1], dp[i-1][0] - price);
```

### 🔹 Interview Tip

If problem says **“at most once / twice / k times”**, this pattern applies.

---

## 3️⃣ Knapsack DP (0/1 & Unbounded)

### 🔹 Pattern

Choose items with constraints.

### 🔹 State

```
dp[w] or dp[i][w]
```

### 🔹 Variants

| Type      | Loop Order |
| --------- | ---------- |
| 0/1       | reverse    |
| Unbounded | forward    |

### 🔹 Problems

* Coin Change I
* Coin Change II
* Partition Equal Subset Sum
* Target Sum

### 🔹 Template (Unbounded)

```java
dp[0] = 1;
for (coin : coins)
    for (i = coin; i <= amount; i++)
        dp[i] += dp[i - coin];
```

### 🔹 Interview Tip

Coins outside loop → **combinations**
Amount outside loop → **permutations**

---

## 4️⃣ Counting DP

### 🔹 Pattern

Count number of valid ways.

### 🔹 Base Case

```
dp[0] = 1
```

### 🔹 Problems

* Coin Change II
* Unique Paths
* Decode Ways
* Count Square Submatrices

### 🔹 Common Mistake

Using `dp[0] = 0` ❌

### 🔹 Interview Tip

If answer is “how many ways”, start with **dp[0] = 1**

---

## 5️⃣ Subsequence DP (Pick / Not Pick)

### 🔹 Pattern

Two choices per element.

### 🔹 State

```
dp[i][j] = answer using first i chars and j chars
```

### 🔹 Problems

* LCS
* Longest Palindromic Subsequence
* Edit Distance
* Distinct Subsequences

### 🔹 Transition

```java
if match:
    dp[i][j] = 1 + dp[i-1][j-1]
else:
    dp[i][j] = max(dp[i-1][j], dp[i][j-1])
```

### 🔹 Interview Tip

Strings + “longest” → **2D DP**

---

## 6️⃣ Subarray DP (Kadane-style)

### 🔹 Pattern

Continuous segment, must include current index.

### 🔹 State

```
dp[i] = best subarray ending at i
```

### 🔹 Problems

* Maximum Subarray
* Maximum Product Subarray
* Longest Turbulent Subarray

### 🔹 Transition

```java
dp[i] = max(nums[i], dp[i-1] + nums[i]);
```

### 🔹 Interview Tip

“Subarray” (contiguous) ≠ “subsequence”

---

## 7️⃣ Grid DP (2D matrix traversal)

### 🔹 Pattern

Move right/down or neighbors.

### 🔹 State

```
dp[i][j] = answer ending at (i,j)
```

### 🔹 Problems

* Unique Paths
* Min Path Sum
* Maximal Square
* Count Square Submatrices

### 🔹 Transition

```java
dp[i][j] = min(top, left, diag) + 1
```

### 🔹 Interview Tip

Matrix + paths/squares → **2D DP**

---

## 8️⃣ Interval DP

### 🔹 Pattern

Solve smaller intervals first.

### 🔹 State

```
dp[l][r] = answer for interval l..r
```

### 🔹 Problems

* Burst Balloons
* Palindrome Partitioning
* Matrix Chain Multiplication

### 🔹 Loop Order

Length → left → right

### 🔹 Interview Tip

If choices split into **left and right parts**, think interval DP.

---

## 9️⃣ LIS-style DP

### 🔹 Pattern

Depends on previous smaller elements.

### 🔹 State

```
dp[i] = LIS ending at i
```

### 🔹 Problems

* LIS
* Russian Doll Envelopes
* Longest Chain Pair

### 🔹 Transition

```java
for j < i:
    if nums[j] < nums[i]:
        dp[i] = max(dp[i], dp[j] + 1)
```

### 🔹 Optimization

Binary search → O(n log n)

---

## 🔟 DP + Binary Search

### 🔹 Pattern

DP state optimized by binary search.

### 🔹 Problems

* Job Scheduling
* LIS (optimized)
* Weighted intervals

### 🔹 Interview Tip

Sorting + compatibility → binary search + DP

---

# 🧠 1-Minute Pattern Recognition Table

| Problem Mentions | Think            |
| ---------------- | ---------------- |
| Ways / count     | Counting DP      |
| Min / Max        | Optimization DP  |
| Subsequence      | 2D DP            |
| Subarray         | Kadane           |
| Coins            | Knapsack         |
| Grid             | Matrix DP        |
| Jobs / intervals | Sort + DP        |
| At most k        | State machine DP |

---
