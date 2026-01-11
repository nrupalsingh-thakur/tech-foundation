# CPU Bottlenecks

## 1. What problem does this solve?
The system feels slow even though:
- Memory is available
- Disk is idle

## 2. Core idea
CPU bottlenecks happen when:
- Too many runnable processes
- Too much computation per request

## 3. Mental model
CPU is a single checkout counter:
- More customers → longer wait
- Faster cashier → higher throughput

## 4. Diagram — CPU contention

        CPU
         │
    ┌────┼────┐
    │ P1 │ P2 │ P3 │ P4 │
    └────┴────┴────┴────┘
        ↑ context switching ↑

## 5. Linux symptoms
- High load average
- High user/system CPU
- Requests queue up

## 6. Connections
- Scheduling (Level 1)
- cgroups CPU limits (Level 4)

