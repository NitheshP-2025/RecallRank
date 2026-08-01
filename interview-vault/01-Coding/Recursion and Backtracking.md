# Recursion and Backtracking

**Definition:** Recursion solves a problem by calling itself on smaller subproblems until a base case; backtracking explores a decision tree of choices and undoes ("backtracks") a choice when it violates a constraint.

**Time/Space Complexity:** Highly problem-dependent; backtracking is often exponential in the worst case (e.g. O(2^n) or O(n!)) since it explores a full decision tree, though pruning cuts this significantly in practice. Space is O(depth of recursion) for the call stack.

**When to use it (pattern cue):** "Generate all," "find all subsets/permutations/combinations," or constraint-satisfaction problems (N-Queens, Sudoku) where you make a choice, recurse, and undo it if it fails.

**Worked micro-example:** Generate all subsets of [1,2].
```
start with []
choose 1: [1] -> choose 2: [1,2] -> backtrack -> [1]
backtrack from 1: []
choose 2: [2]
Result: [], [1], [1,2], [2]
```

**Common interview variant / gotcha:** Forgetting to actually "undo" the choice (e.g. popping from a path list) before trying the next branch, which silently corrupts later results; not identifying the base case clearly enough, causing infinite recursion or missed results.
