# OS - Deadlocks and Synchronization

**Key points / formula:** Deadlock requires all 4 conditions simultaneously: Mutual Exclusion, Hold and Wait, No Preemption, Circular Wait. Breaking any one prevents deadlock. Synchronization tools: mutex (mutual exclusion lock, one owner), semaphore (counter-based, allows N concurrent accesses).

**When it's asked (pattern cue):** "What causes a deadlock and how do you prevent it," or "difference between mutex and semaphore."

**Worked micro-example:** Two processes each hold one resource and wait for the other's resource -> circular wait -> deadlock. Prevention: enforce a strict global ordering on resource acquisition so circular wait can't form.

**Common gotcha / trick:** Saying mutex and (binary) semaphore are "the same thing" — the key difference is ownership: a mutex can only be released by the thread that locked it, while a semaphore can be signaled by any thread, which matters for signaling between different threads.
