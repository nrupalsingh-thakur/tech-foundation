## 13 — HTTP (Built on TCP, Not Magic)

### What HTTP Really Is

HTTP is:
- a text protocol
- over TCP
- with strict rules

Nothing more.

---

### Request / Response

Client Server

HTTP request -------------> parse
HTTP response <------------- reply

---

### Headers

Headers are metadata:
- content type
- auth info
- instructions

They exist because:
- TCP only moves bytes
- HTTP adds meaning

---

### Status Codes

Status codes answer:
> “What happened?”

- `2xx` success
- `3xx` redirect
- `4xx` client error
- `5xx` server error

Clear communication.

---

### Keep-Alive

Creating TCP connections is expensive.

Keep-alive:
- reuses one connection
- for many requests

This improves:
- performance
- latency
- resource usage

---

## Final Mental Model

Networking is:
- OS-managed I/O
- byte movement
- layered problem-solving

Each layer exists for a reason.
Once you see the layers, behavior stops being mysterious.
