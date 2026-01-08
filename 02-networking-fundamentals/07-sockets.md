## 07 — Sockets (The OS Object That Matters)

### What a Socket Is

A socket is:
> an OS-managed object representing a network endpoint

Same category as:
- files
- pipes
- devices

Process

|

v

[file descriptor]

|

v

socket -> kernel -> network

Key insight:
- Networking is **I/O**
- Not special
- Not magical

You read and write sockets like files.
