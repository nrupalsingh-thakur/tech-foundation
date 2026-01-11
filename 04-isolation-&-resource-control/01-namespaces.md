# Namespaces

## 1. What problem does this solve?
Processes could see everything on the system.
Isolation did not exist.

## 2. Core idea
Namespaces control **what a process can see**.

## 3. Mental model
The kernel shows each process a **custom view of reality**.

## 4. Diagram — visibility isolation

Before namespaces:

    Process A ──┐
    Process B ──┼── sees all processes, network, filesystem
    Process C ──┘

After namespaces:

    ┌──────────── Namespace 1 ────────────┐
    │  Process A   Process B              │
    └─────────────────────────────────────┘

    ┌──────────── Namespace 2 ────────────┐
    │  Process C                          │
    └─────────────────────────────────────┘

## 5. Important namespace types
- PID → which processes you see
- Network → IPs, ports, routes
- Mount → filesystem view
- UTS → hostname

## 6. Linux symptoms
- `ps` shows fewer processes
- Same ports reused safely
- `/` looks different per container

## 7. Connections
- Isolation only, no limits
- cgroups are still required

