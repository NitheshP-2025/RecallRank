# OS - Process and Threads

**Key points / formula:** A process is an independent program in execution with its own memory space; a thread is a lightweight unit of execution within a process, sharing the process's memory but with its own stack and registers. Context switching between processes is more expensive than between threads (more state to save/restore).

**When it's asked (pattern cue):** "Difference between process and thread," "what is context switching," or multithreading/concurrency design questions.

**Worked micro-example:** A web browser is one process; each tab may run as a separate thread (or process, in modern browsers) sharing/isolating memory depending on the architecture — explains why one crashed tab doesn't always crash the whole browser.

**Common gotcha / trick:** Saying threads "don't share memory" (they do — that's the whole point, and also the source of race conditions); not being able to explain WHY thread switching is cheaper than process switching (less state, no full memory-map reload).
