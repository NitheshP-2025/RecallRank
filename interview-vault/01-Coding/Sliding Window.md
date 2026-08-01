# Sliding Window

**Definition:** Maintains a subrange ("window") over an array or string that expands or contracts based on a condition, avoiding recomputation from scratch at each position.

**Time/Space Complexity:** O(n) time (each element enters and leaves the window at most once), O(1) or O(k) extra space depending on what the window tracks (e.g. a frequency map).

**When to use it (pattern cue):** Problems about a "contiguous subarray/substring" with a max/min length, or a running sum/count/frequency condition — especially with the words "longest," "shortest," or "at most k" in a contiguous range.

**Worked micro-example:** Longest substring without repeating characters, "abcabcbb".
```
window expands: a,b,c (all unique, length 3)
hit repeat 'a' -> shrink window from left until 'a' removed
continue expanding/shrinking, tracking max length seen = 3
```

**Common interview variant / gotcha:** Confusing "fixed-size window" problems (window size is given) with "variable-size window" problems (window grows/shrinks based on a condition) — they use different loop structures; forgetting to update the tracking structure (e.g. frequency map) when shrinking the window, not just when expanding it.
