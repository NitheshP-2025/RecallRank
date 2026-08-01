# DBMS - Normalization and Keys

**Key points / formula:** Normalization removes redundancy: 1NF (atomic values, no repeating groups), 2NF (1NF + no partial dependency on a composite key), 3NF (2NF + no transitive dependency), BCNF (stricter 3NF for edge cases with overlapping candidate keys). Keys: Primary key (unique identifier), Candidate key (any column set that could be primary), Foreign key (references another table's primary key).

**When it's asked (pattern cue):** "Normalize this table to 3NF," or "what's the difference between a candidate key and a primary key," or general schema-design questions.

**Worked micro-example:** A table storing (StudentID, CourseID, CourseName) has CourseName depending only on CourseID, not the full key (StudentID+CourseID) — a partial dependency, violating 2NF. Fix: split into (StudentID, CourseID) and (CourseID, CourseName).

**Common gotcha / trick:** Over-normalizing to the point of hurting query performance (real systems often deliberately denormalize for read-heavy workloads) — be ready to discuss this tradeoff, not just recite normal forms; confusing a foreign key (a reference) with a candidate key (a uniqueness property).
