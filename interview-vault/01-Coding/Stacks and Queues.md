# Stacks and Queues

**Definition:** A stack is LIFO (last in, first out); a queue is FIFO (first in, first out) — both used to control the order in which elements are processed.

**Time/Space Complexity:** O(1) for push/pop (stack) or enqueue/dequeue (queue) with proper implementation (array-backed with amortized resizing, or linked list); O(n) space for n elements.

**When to use it (pattern cue):** Stack: matching/balancing problems (parentheses), "undo" operations, DFS iterative implementation, expression evaluation. Queue: BFS traversal, task scheduling, anything processed in arrival order.

**Worked micro-example:** Valid parentheses check with a stack.
```
"{[()]}"
{ -> push, stack=[{]
[ -> push, stack=[{,[]
( -> push, stack=[{,[,(]
) -> matches top ( -> pop, stack=[{,[]
] -> matches top [ -> pop, stack=[{]
} -> matches top { -> pop, stack=[]
Empty at end -> valid
```

**Common interview variant / gotcha:** Using a stack where a queue was needed (or vice versa) because the problem's "process in order" requirement wasn't read carefully — always double check whether the intended traversal is depth-first (stack) or breadth-first (queue) before starting.
