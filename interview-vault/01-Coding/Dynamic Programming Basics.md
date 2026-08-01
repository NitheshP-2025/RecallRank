# Dynamic Programming Basics

**Definition:** Breaks a problem into overlapping subproblems, storing results (memoization top-down, or tabulation bottom-up) to avoid recomputation.

**Time/Space Complexity:** Varies by problem, but typically reduces exponential brute force (e.g. O(2^n) recursion) down to O(n) or O(n^2) time, with O(n) or O(n^2) space for the memo/table (sometimes reducible to O(1) with rolling variables).

**When to use it (pattern cue):** The problem asks for "number of ways," "minimum/maximum," or "is it possible" AND naive recursion re-solves the same subproblem multiple times (check: does a recursion tree have repeated calls with the same arguments?).

**Worked micro-example:** Fibonacci with memoization.
```
fib(5) calls fib(4)+fib(3)
fib(4) calls fib(3)+fib(2)  <- fib(3) repeated, cache it
memo = {0:0, 1:1}
fib(2)=1, fib(3)=2, fib(4)=3, fib(5)=5 (each computed once, cached)
```

**Common interview variant / gotcha:** Jumping straight to code without first defining the state (what does dp[i] mean?) and the transition (how does dp[i] relate to smaller states?) — interviewers weight this reasoning step heavily; also forgetting base cases, which silently break the recurrence.
