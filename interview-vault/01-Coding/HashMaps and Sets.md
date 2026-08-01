# HashMaps and Sets

**Definition:** Key-value (map) or unique-value (set) structures backed by a hash function, giving average O(1) lookup, insert, and delete by trading space for speed.

**Time/Space Complexity:** O(1) average for get/put/contains; O(n) worst case with heavy hash collisions (rare in practice with good hash functions). Space is O(n) for n stored elements.

**When to use it (pattern cue):** Need to check "have I seen this before," count frequencies, or look up a complement value in O(1) instead of scanning — classic swap-in for any O(n^2) nested-loop "does a pair exist" problem.

**Worked micro-example:** Two Sum using a hashmap.
```
arr = [2, 7, 11, 15], target = 9
seen = {}
i=0: 2, need 7, not in seen -> seen={2:0}
i=1: 7, need 2, 2 IS in seen -> return (0, 1)
```

**Common interview variant / gotcha:** Assuming O(1) is guaranteed rather than average-case (worst case degrades to O(n) with pathological collisions); forgetting that iteration order isn't guaranteed in a plain hashmap (use a LinkedHashMap/OrderedDict if order matters).
