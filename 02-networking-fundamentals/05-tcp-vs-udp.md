## 05 — TCP vs UDP (Reliability Choices)

### Why Two Protocols Exist

Different problems need different tradeoffs.

---

### UDP — Speed First

**Mental model:**  
Shouting updates during a live sports game.

Properties:
- No connection
- No guarantees
- Very fast
- Very simple

Used when:
- losing data is acceptable
- speed matters more than correctness

Examples:
- video calls
- games
- DNS

send packet
move on

---

### TCP — Correctness First

**Mental model:**  
Registered mail with receipts.

TCP guarantees:
- delivery
- ordering
- retries
- flow control

The OS handles all of this.

Used when:
- correctness matters
- developers want simplicity

Examples:
- HTTP
- SSH
- databases

send bytes
OS manages packets
receive bytes

yaml
Copy code

TCP hides packet chaos from you.
