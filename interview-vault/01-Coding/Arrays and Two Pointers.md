Arrays and Two Pointers

Definition: Contiguous memory blocks accessed by index; the two-pointer technique uses two indices moving toward or away from each other to avoid nested loops.

Time/Space Complexity: Array access is O(1); two-pointer scans are typically O(n) time, O(1) extra space (vs O(n^2) brute force with nested loops).

When to use it (pattern cue): Sorted array + looking for a pair/triplet matching a condition (sum, difference); removing duplicates in place; reversing/partitioning in place; problems mentioning "sorted" and "pair" together.

Worked micro-example: Find two numbers in a sorted array that sum to a target.
```
arr = [1, 3, 4, 6, 8], target = 10
left=0 (1), right=4 (8) -> sum=9 < 10 -> left++
left=1 (3), right=4 (8) -> sum=11 > 10 -> right--
left=1 (3), right=3 (6) -> sum=9 < 10 -> left++
left=2 (4), right=3 (6) -> sum=10 -> found (4, 6)
```

Common interview variant / gotcha: Forgetting the array must be sorted first for the classic left/right pointer pattern; confusing this with the "fast/slow pointer" variant used for cycle detection in linked lists (different problem class, same name "two pointers").
