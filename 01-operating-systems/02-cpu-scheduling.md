# 2. CPU Scheduling & Load

### Intuition

The CPU is **scarce**.

The OS decides:

- Who runs
- For how long
- In what order

This decision process is **CPU scheduling**.

------

### Key Concepts

#### CPU Time Sharing

The OS slices CPU time into tiny chunks and distributes them.

You *feel* parallelism — but it’s mostly illusion.

------

#### Load Average

Load average answers:

> “How many things *want* the CPU?”

- Load = 1 → one task fully using CPU
- Load > CPU cores → system feels slow

High load ≠ high CPU usage
 It often means **things are waiting**.

------

#### Blocking vs Running

- Running → actively using CPU
- Blocking → waiting for disk, network, memory

Blocked processes still count toward load.

------

#### Priority & Nice

Each process has a **priority**.

- High priority → runs sooner
- Low priority → waits longer

`nice` lets you be polite to other processes.

------

### Mental Model

> CPU slowness is not about speed — it’s about **competition**.