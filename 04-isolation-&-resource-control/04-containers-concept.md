i# Containers — Conceptual View

## 1. What containers are
Containers are **not VMs**.
They are **isolated process groups**.

## 2. Diagram — container anatomy

            ┌─────────────────────────────┐
            │        Linux Kernel          │
            │  (namespaces + cgroups)     │
            └───────────▲─────────────────┘
                        │
        ┌───────────────┴───────────────┐
        │           Container           │
        │                               │
        │  Process 1                    │
        │  Process 2                    │
        │  Process 3                    │
        │                               │
        │  - Namespaces (isolation)     │
        │  - cgroups (limits)           │
        └───────────────────────────────┘

## 3. Why containers are fast
- No guest OS
- No hardware emulation
- Direct kernel usage

## 4. Key truth (memorize this)
Containers = processes + kernel features

## 5. Connections
- Built on OS fundamentals
- Orchestrated by higher layers later

