# Memory Bottlenecks

## 1. What problem does this solve?
Sudden crashes, OOM kills, or heavy swapping.

## 2. Core idea
Memory bottlenecks happen when:
- Working set > available RAM
- Allocation grows without release

## 3. Mental model
Memory is a desk:
- Too many papers → things fall off
- OS starts moving papers to the floor (swap)

## 4. Diagram — memory pressure

        RAM (Full)
    ┌────────────────┐
    │ App Data       │
    │ Cache          │
    │ Stack/Heap     │
    └───────▲────────┘
            │
        OOM Killer

## 5. Linux symptoms
- Swap usage
- OOM kill messages
- Sudden process death

## 6. Connections
- Virtual memory (Level 1)
- cgroups memory limits (Level 4)

