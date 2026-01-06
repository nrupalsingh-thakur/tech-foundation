# 3. Memory Management

### Intuition

Memory is **finite**.

The OS must:

- Give memory to processes
- Take it back
- Pretend there’s more than actually exists

This illusion is called **virtual memory**.

------

### Key Concepts

#### Virtual Memory

Each process believes:

> “I have my own huge memory space”

Reality:

- OS maps virtual memory → physical RAM
- Keeps processes isolated

------

#### RAM vs Swap

- RAM → fast, limited
- Swap → slow, disk-based overflow

Swap prevents crashes but causes slowness.

------

#### Page Cache

The OS:

- Remembers recently used disk data
- Keeps it in memory

This is why:

- Second file read is faster
- Free memory ≠ unused memory

------

#### OOM Killer

When memory runs out:

> The OS **kills a process** to survive

It doesn’t ask.
 It chooses what seems least important.

------

### Mental Model

> Memory problems don’t fail gracefully — they **explode suddenly**.