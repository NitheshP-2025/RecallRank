# DBMS - Transactions and ACID

**Key points / formula:** ACID: Atomicity (all-or-nothing — a transaction fully completes or fully rolls back), Consistency (database moves from one valid state to another, respecting constraints), Isolation (concurrent transactions don't interfere with each other's intermediate state), Durability (once committed, changes survive even a crash).

**When it's asked (pattern cue):** "Explain ACID properties," or "what isolation level would you use for X scenario" (dirty reads, phantom reads).

**Worked micro-example:** A bank transfer debits account A and credits account B. Atomicity ensures that if the credit step fails after the debit succeeds, the whole transaction rolls back — money isn't lost mid-transfer.

**Common gotcha / trick:** Confusing Consistency (database-level constraint validity) with Isolation (transaction-level concurrency control) — they sound similar but solve different problems; not knowing that higher isolation levels (Serializable) trade off performance for stricter concurrency guarantees.
