## 01 — What a Network Is

### Mental Model

A network is **not** the internet.

A network is:
- a system for delivering bytes
- between machines
- using agreed rules

Process A OS A Network OS B Process B

bytes ---> socket -> packets -> socket ---> bytes

Key insight:
- Processes never “talk to the network”
- They talk to the **OS**
- The OS talks to the network

Same pattern as files.
