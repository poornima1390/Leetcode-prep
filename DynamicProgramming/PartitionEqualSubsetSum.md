

## 1️⃣ What am I optimizing / counting / deciding?

> **Deciding true or false**

This is a **decision DP** problem:

* Can we pick a subset whose sum = `totalSum / 2`?

No optimization, no counting — just feasibility.

---

## 2️⃣ What is the DP state?

> **dp[target + 1]**

### Correct DP State

```
dp[s] = true if some subset of processed numbers can make sum s
```

* `target = totalSum / 2`
* DP size = `target + 1`
* This is **0/1 Knapsack feasibility**

## 3️⃣ What is the transition?

For each number `num`:

```
dp[s] = dp[s] OR dp[s - num]
```

(only if `s >= num`)

Meaning:

* Either we **don’t take** `num`
* Or we **take** `num` and previously we could make `s - num`

This is the classic **pick / not pick** transition.

---

## 4️⃣ What is the base case?

> **dp[0] = true**

✅ **100% correct**

Why?

* Sum `0` is always achievable by picking nothing.

This base case is **non-negotiable**.

---

## 5️⃣ Does loop order matter?

> **Yes: outer loop nums, inner loop dp**

### Correct Loop Order

```java
for (num : nums) {
    for (s = target; s >= num; s--) {
        dp[s] = dp[s] || dp[s - num];
    }
}
```

### Why reverse order?

* Prevents reusing the same number multiple times
* Enforces **0/1 constraint**

If you loop forward → ❌ turns into unbounded knapsack (wrong)

> “This is a decision DP problem. I reduce it to checking if a subset sums to totalSum/2.
> I use a 1D boolean DP where dp[s] means whether sum s is achievable using some of the numbers seen so far.
> The transition is dp[s] |= dp[s - num], iterating sums backward to avoid reusing numbers.”

Time complexity: O(nums.length * target)
Space Complexity: O(target)
