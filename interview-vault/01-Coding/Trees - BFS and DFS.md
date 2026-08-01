# Trees - BFS and DFS

**Definition:** Traversal strategies for hierarchical structures: BFS explores level by level using a queue, DFS explores as deep as possible along one branch first using a stack or recursion.

**Time/Space Complexity:** Both are O(n) time (visit every node once). Space: BFS is O(width of tree) for the queue (worst case O(n) for a wide/complete tree); DFS is O(height of tree) for the recursion stack (worst case O(n) for a skewed tree, O(log n) for a balanced tree).

**When to use it (pattern cue):** BFS: "shortest path," "level order," "minimum steps" in an unweighted tree/graph. DFS: "all paths," "does a path exist," subtree computations, or when you need to explore fully before backtracking (e.g. validating a BST).

**Worked micro-example:** Level order (BFS) on a tree with root 1, children 2 and 3.
```
queue = [1]
pop 1, visit, push children -> queue = [2, 3]
pop 2, visit, push children (none) -> queue = [3]
pop 3, visit, push children (none) -> queue = []
Order visited: 1, 2, 3
```

**Common interview variant / gotcha:** Confusing the three DFS orders (pre-order, in-order, post-order) and using the wrong one for the problem (e.g. in-order gives sorted output for a BST, but only in-order); forgetting that BFS needs an explicit queue while DFS can be done with simple recursion (implicit call stack) or an explicit stack.
