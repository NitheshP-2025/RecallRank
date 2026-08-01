# Computer Networks - OSI and TCP-IP

**Key points / formula:** OSI has 7 layers (Physical, Data Link, Network, Transport, Session, Presentation, Application). TCP/IP is the practical 4-layer model (Link, Internet, Transport, Application) that real-world networking actually implements. TCP is connection-oriented and reliable (retransmits lost packets); UDP is connectionless and faster but unreliable.

**When it's asked (pattern cue):** "Explain the OSI model layers," "TCP vs UDP," or "what happens when you type a URL into a browser" (a classic full-stack walkthrough question).

**Worked micro-example:** A video call uses UDP (occasional dropped frames are acceptable, low latency matters more) while a file download uses TCP (every byte must arrive correctly, some latency is acceptable).

**Common gotcha / trick:** Reciting all 7 OSI layers without being able to map them to TCP/IP's 4 layers or explain why TCP/IP is what's actually used in practice; not knowing a concrete example of when UDP is preferred over TCP despite being "less reliable."
