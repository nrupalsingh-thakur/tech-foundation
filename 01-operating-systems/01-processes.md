# 1. Processes & Threads

### Intuition

A **process** is:

> A running program + its own memory + OS tracking info

When you run:

```
python app.py
```

The OS creates a **process**.

A **thread** is:

> A smaller unit of execution *inside* a process

Think:

- Process = house
- Threads = people inside the house sharing rooms

------

### Why This Matters

Everything running on your computer is a **process**:

- Browser
- Terminal
- Server
- Background services

If you don’t understand processes, nothing else makes sense.

------

### Key Concepts

#### Process Lifecycle

A process usually goes through:

1. Created
2. Running
3. Waiting (blocked on I/O)
4. Terminated

The OS constantly moves processes between these states.

------

#### Threads vs Processes

| Feature      | Process  | Thread                 |
| ------------ | -------- | ---------------------- |
| Memory       | Separate | Shared                 |
| Isolation    | Strong   | Weak                   |
| Crash impact | Local    | Can kill whole process |
| Speed        | Slower   | Faster                 |

Threads are faster — but more dangerous.

------

#### Context Switching

The CPU can only run **one thing per core**.

So the OS:

- Pauses Process A
- Saves its state
- Loads Process B
- Runs it

This is called a **context switch**.

Too many context switches = slow system.

------

#### Signals

Signals are:

> The OS tapping a process on the shoulder

Examples:

- `SIGKILL` → die immediately
- `SIGTERM` → please shut down nicely
- `SIGINT` → Ctrl+C

------

### Mental Model

> Your computer is not “slow” — it’s **busy switching attention**.