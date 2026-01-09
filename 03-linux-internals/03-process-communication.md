## 12. Process Communication

Processes are isolated to keep the system stable and secure.

However, real systems need processes to cooperate.

Linux provides **Inter-Process Communication (IPC)**.

---

### Pipes

A pipe connects the output of one process to the input of another.

Example:
ls | grep ".txt"

Conceptually:
[Process A] ─────▶ [Process B]

- One process writes data
- The other reads it

Used for chaining commands.

---

### Signals

Signals are small messages sent to a process.

Examples:
- `SIGINT` (Ctrl + C)
- `SIGTERM`
- `SIGKILL`

Concept:
Event → Signal → Process reacts

Used to:
- Stop processes
- Restart services
- Reload configurations

---

### Shared Memory (Conceptual)

Used when large amounts of data need to be shared efficiently.

Instead of copying data:
- Multiple processes map the same memory region

Concept:
Process A
│
├── Shared Memory ──┤
│ │
Process B

Used in:
- Databases
- High-performance systems

---

## Level 3 Summary

Boot process
↓
systemd
↓
Services
↓
Processes
↓
Permissions & security
↓
Process communication


After Level 3:
- Linux behavior feels logical
- System structure becomes predictable
- You understand *why* things work, not just *how*
