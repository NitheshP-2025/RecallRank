# Graphs - BFS and DFS

**Definition:** Traversal of nodes and edges in a graph (which, unlike trees, can have cycles and multiple paths between nodes); BFS explores level by level via a queue, DFS explores as deep as possible via a stack or recursion.

**Time/Space Complexity:** O(V + E) time for both (visit every vertex and edge once), where V = vertices, E = edges. Space: O(V) for the visited set plus O(V) for the queue (BFS) or recursion stack (DFS) in the worst case.

**When to use it (pattern cue):** BFS: shortest path in an unweighted graph, "minimum number of steps/moves," level-by-level spread (e.g. rotting oranges, word ladder). DFS: detecting cycles, connected components, topological sort, "does a path exist between A and B," or exhaustive exploration (islands, flood fill).

**Worked micro-example:** BFS shortest path from node 1 to node 4 in graph {1:[2,3], 2:[4], 3:[4]}.
```
queue = [1], visited = {1}, dist = {1:0}
pop 1 -> neighbors 2,3 -> queue=[2,3], dist={2:1,3:1}
pop 2 -> neighbor 4 -> queue=[3,4], dist={4:2}
pop 3 -> neighbor 4 already visited -> skip
pop 4 -> done. Shortest distance to 4 = 2
```

**Common interview variant / gotcha:** Forgetting to mark nodes as visited before (not after) adding them to the queue in BFS, which causes the same node to be enqueued multiple times; not handling disconnected graphs (looping over all unvisited nodes to run DFS/BFS on each component); confusing "shortest path" (needs BFS on unweighted graphs, or Dijkstra on weighted ones) with "does a path exist" (either BFS or DFS works).
