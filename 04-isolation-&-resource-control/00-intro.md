# Level 4 — Isolation & Resource Control

## 1. What problem does this level solve?
Running many applications on the same OS safely and efficiently.

## 2. Core idea
The Linux kernel provides:
- Namespaces → isolation (what a process can see)
- cgroups → limits (what a process can use)

Containers are built from these.

## 3. Big picture diagram

                ┌─────────────────────────┐
                │        Hardware         │
                └───────────▲─────────────┘
                            │
                ┌───────────┴─────────────┐
                │        Linux Kernel      │
                │  (namespaces + cgroups) │
                └───────▲────────▲────────┘
                        │        │
              ┌─────────┘        └─────────┐
        ┌───────────────┐        ┌───────────────┐
        │   Container A │        │   Container B │
        │  (processes) │        │  (processes) │
        └───────────────┘        └───────────────┘

All containers share **one kernel**.

## 4. Why this matters
Without this:
- Containers would be impossible
- Cloud systems would waste massive resources

## 5. Connections
- Built on processes
- Enables Docker and Kubernetes

