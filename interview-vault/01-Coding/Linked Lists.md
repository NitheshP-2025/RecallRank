# Linked Lists

**Definition:** A sequence of nodes connected via pointers (not contiguous memory), enabling O(1) insertion/deletion once you're at the right node.

**Time/Space Complexity:** O(n) to search/access by position (no random access like arrays), O(1) to insert/delete at a known node, O(n) space for n nodes.

**When to use it (pattern cue):** Problems mentioning "reverse," "detect a cycle," "merge two sorted lists," or "find the middle" — anything where you traverse once and need O(1) pointer manipulation instead of shifting array elements.

**Worked micro-example:** Detect a cycle with fast/slow pointers (Floyd's algorithm).
```
slow moves 1 step, fast moves 2 steps
If there's a cycle, fast eventually laps slow and they meet at the same node
If fast reaches null, there's no cycle
```

**Common interview variant / gotcha:** Losing the reference to the next node before rewiring pointers during a reversal (classic bug: `curr.next = prev` before saving `next = curr.next` first); forgetting to handle the empty list or single-node edge cases.
