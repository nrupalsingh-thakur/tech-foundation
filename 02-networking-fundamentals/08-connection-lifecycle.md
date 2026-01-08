## 08 — Connection Lifecycle (What Actually Happens)

### TCP Connection Steps

Client Server

socket() socket()
connect() ------------------> accept()
send/recv <-----------------> send/recv
close() close()

Each step:
- is a syscall
- involves kernel state
- consumes resources

Connections are real OS objects.
