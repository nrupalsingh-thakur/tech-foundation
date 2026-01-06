# 5. System Calls & OS Interface

### Intuition

Programs **cannot touch hardware directly**.

They must ask the OS politely.

That request is a **system call**.

------

### Key Concepts

#### What System Calls Are

Examples:

- `read()`
- `write()`
- `fork()`
- `open()`

They are the **boundary** between:

- User space (your code)
- Kernel space (OS)

------

#### Blocking vs Non-Blocking I/O

- Blocking → wait until done
- Non-blocking → continue, check later

This affects:

- Performance
- Scalability
- Responsiveness

------

### Mental Model

> Programs don’t control the machine — **the OS does**.