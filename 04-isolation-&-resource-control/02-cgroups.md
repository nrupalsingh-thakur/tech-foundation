# cgroups (Control Groups)

## 1. What problem does this solve?
Processes could consume unlimited resources and crash systems.

## 2. Core idea
cgroups control **how much a process can use**.

## 3. Mental model
Resource budgeting enforced by the kernel.

## 4. Diagram — resource control

                    CPU / Memory / Disk
                            ▲
                            │
                ┌───────────┴───────────┐
                │        Kernel          │
                │        (cgroups)       │
                └───────▲────────▲──────┘
                        │        │
              ┌─────────┘        └─────────┐
        ┌───────────────┐        ┌───────────────┐
        │   Process A   │        │   Process B   │
        │   CPU: 20%    │        │   CPU: 80%    │
        │   Mem: 512MB  │        │   Mem: 2GB    │
        └───────────────┘        └───────────────┘

Kernel enforces limits automatically.

## 5. What happens on limit breach
- CPU → throttled
- Memory → OOM kill
- System survives

## 6. Connections
- Works alongside namespaces
- Critical for container safety

