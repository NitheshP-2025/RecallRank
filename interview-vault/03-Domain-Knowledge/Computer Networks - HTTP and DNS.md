# Computer Networks - HTTP and DNS

**Key points / formula:** DNS resolves a domain name to an IP address (via a hierarchy of resolvers, root/TLD/authoritative servers). HTTP is a stateless request-response protocol; HTTPS adds TLS encryption on top. Common status codes: 200 (OK), 301/302 (redirect), 404 (not found), 500 (server error).

**When it's asked (pattern cue):** "What happens when you type a URL and press enter" (walks through DNS lookup, TCP handshake, HTTP request/response, rendering) — a very common full-stack conceptual question.

**Worked micro-example:** Typing "example.com" -> browser checks DNS cache -> if miss, queries a resolver -> resolver walks root -> TLD -> authoritative server -> returns IP -> browser opens a TCP connection to that IP and sends an HTTP GET request.

**Common gotcha / trick:** Forgetting DNS results are cached at multiple levels (browser, OS, ISP resolver) which is why DNS changes can take time to "propagate"; not mentioning the TLS handshake step when explaining HTTPS specifically (it's not just "HTTP but encrypted" — there's a real negotiation step first).
