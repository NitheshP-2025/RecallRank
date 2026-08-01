# Heaps and Priority Queues

**Definition:** A tree-based structure (usually a binary heap) that keeps the min or max element at the root, giving fast access to the "next most important" item.

**Time/Space Complexity:** O(log n) for insert/delete, O(1) to peek the min/max, O(n) space. Building a heap from an unsorted array is O(n).

**When to use it (pattern cue):** "Top-k" or "k-th largest/smallest" problems, merging k sorted lists, scheduling by priority, or any problem needing repeated access to the current min/max as the data changes.

**Worked micro-example:** Find the 3rd largest element using a min-heap of size 3.
```
arr = [7, 10, 4, 3, 20, 15]
Keep a min-heap of size 3 as you scan:
after processing: heap = [10, 15, 20] (min-heap, root=10)
root of the heap (10) is the 3rd largest overall
```

**Common interview variant / gotcha:** Mixing up min-heap vs max-heap for the problem's direction (e.g. using a max-heap when you actually need to evict the largest to keep only the k smallest); most languages' built-in heap is a min-heap by default, so max-heap behavior needs negation or a custom comparator.
