# Sorting Algorithms

**Definition:** Methods for ordering data by comparison (e.g. merge sort, quicksort) or non-comparison (e.g. counting sort, radix sort) means, each with different time/space/stability tradeoffs.

**Time/Space Complexity:** Comparison sorts: O(n log n) average (merge sort, quicksort, heapsort); O(n^2) worst case for quicksort with a bad pivot. Merge sort: O(n) space, always stable. Quicksort: O(log n) space, in-place, not stable. Counting/radix sort: O(n+k) time, not comparison-based.

**When to use it (pattern cue):** Whenever the problem is easier once data is ordered (search, two-pointer, greedy selection), or when directly asked to implement/compare sorting algorithms and their tradeoffs.

**Worked micro-example:** Merge sort splits and merges.
```
[5,2,4,1] -> split -> [5,2] [4,1]
-> split -> [5][2] [4][1]
-> merge -> [2,5] [1,4]
-> merge -> [1,2,4,5]
```

**Common interview variant / gotcha:** Being asked "why quicksort over merge sort" and not knowing the answer is space (quicksort is in-place) vs stability/worst-case guarantees (merge sort is stable and always O(n log n)); not knowing when a non-comparison sort (counting sort) beats O(n log n) for bounded-range integers.
