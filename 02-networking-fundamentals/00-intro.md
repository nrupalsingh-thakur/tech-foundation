# LEVEL 2 — Networking (Built on OS Concepts)

> Goal: Networking should feel like **shipping goods between factories**, not magic spells.

You already know:
- Processes do work
- The OS schedules them
- Files and pipes move bytes *inside* one machine

Networking is how the OS moves bytes **between machines**.

---

## 00 — Big Picture: What Networking Is

### The Core Idea

**A network lets processes on different machines exchange bytes.**

That’s it.

Everything else (DNS, HTTP, TCP) exists because of **constraints**:
- machines crash
- cables drop data
- many programs run at once
- humans hate numbers

---

### Real-World Analogy

Think of:
- Each **machine** as a warehouse
- Each **process** as a worker inside the warehouse
- The **network** as the road system
- The **OS** as the shipping department

Workers don’t touch roads directly.  
They ask shipping to move boxes.

That’s networking.

