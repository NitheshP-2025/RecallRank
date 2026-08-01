# System Design Basics

**Key points / formula:** Core building blocks: load balancer (distributes traffic), cache (reduces repeated expensive reads, e.g. Redis), horizontal scaling (more machines) vs vertical scaling (bigger machine), database choice (SQL for strong consistency/relations, NoSQL for scale/flexible schema), CAP theorem (a distributed system can only fully guarantee 2 of Consistency, Availability, Partition tolerance at once).

**When it's asked (pattern cue):** Open-ended "design a URL shortener / rate limiter / chat system" questions — usually at the end of an interview, testing breadth over depth.

**Worked micro-example:** Designing a URL shortener: hash the long URL to a short code, store the mapping in a fast key-value store (cache-first reads), use a load balancer in front of multiple stateless API servers so traffic scales horizontally.

**Common gotcha / trick:** Jumping straight to a specific technology (e.g. "I'll use Redis") without first stating requirements and constraints (expected scale, read/write ratio, latency needs) — interviewers weight the requirements-gathering step as much as the final design.
