# Binary Search

**Definition:** Halves the search space each step on a sorted structure to find a target or a boundary condition, in O(log n).

**Time/Space Complexity:** O(log n) time, O(1) space (iterative) or O(log n) space (recursive, due to call stack).

**When to use it (pattern cue):** Data is sorted, or the problem has a monotonic condition (a "yes/no" answer that flips exactly once as you scan) — this includes "search on answer" problems like minimizing/maximizing a value under a constraint.

**Worked micro-example:** Find target=6 in [1,3,4,6,8,9].
```
low=0, high=5, mid=2 (4) -> 4 < 6 -> low=3
low=3, high=5, mid=4 (8) -> 8 > 6 -> high=3
low=3, high=3, mid=3 (6) -> found at index 3
```

**Common interview variant / gotcha:** Off-by-one errors in the `low <= high` vs `low < high` loop condition; forgetting `mid = low + (high-low)/2` to avoid integer overflow in languages with fixed-size ints; applying it on unsorted data without realizing the monotonic property still holds (search-on-answer problems).
