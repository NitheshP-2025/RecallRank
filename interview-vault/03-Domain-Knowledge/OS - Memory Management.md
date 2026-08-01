# OS - Memory Management

**Key points / formula:** Paging divides memory into fixed-size pages (avoids external fragmentation but can have internal fragmentation); Segmentation divides by logical units (variable size, can have external fragmentation). Virtual memory lets a process use more memory than physically available RAM by swapping pages to disk (page faults occur when a needed page isn't in RAM).

**When it's asked (pattern cue):** "Explain paging vs segmentation," "what is a page fault," or "how does virtual memory work."

**Worked micro-example:** A process wants to access an address not currently in RAM -> triggers a page fault -> OS pauses the process, loads the required page from disk into RAM (possibly evicting another page via an algorithm like LRU), then resumes execution.

**Common gotcha / trick:** Saying paging has "no fragmentation" (it avoids external fragmentation but still has internal fragmentation from unused space in the last page); not being able to name a page replacement algorithm (LRU, FIFO, Optimal) when asked how the OS decides what to evict.
