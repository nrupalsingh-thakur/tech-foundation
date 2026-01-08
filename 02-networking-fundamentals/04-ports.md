## 04 — Ports (Finding the Right Process)

### The Problem

One machine runs many programs.

When a packet arrives:
- Which process gets it?

---

### The Solution: Ports

**Mental model:**
- IP = apartment building
- Port = apartment number

Machine: 192.168.1.10

Port 22 -> SSH process
Port 80 -> Web server
Port 5432 -> Database

csharp
Copy code

A network endpoint is:
(IP address, port)

That maps to **one socket** inside the OS.
