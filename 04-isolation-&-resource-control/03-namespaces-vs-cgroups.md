# Namespaces vs cgroups

## 1. The confusion
They are often mixed up.
They do different jobs.

## 2. Diagram — side by side

Namespaces (visibility):

    ┌──────────────┐
    │ Process sees │
    │ only its     │
    │ own world    │
    └──────────────┘

cgroups (limits):

    ┌──────────────┐
    │ Process uses │
    │ limited CPU  │
    │ and memory   │
    └──────────────┘

## 3. Key distinction

| Feature     | Namespace        | cgroup            |
|------------|------------------|-------------------|
| Controls   | What you see     | What you use      |
| Purpose    | Isolation        | Resource safety   |

## 4. Why containers need both
Isolation without limits is dangerous.
Limits without isolation are messy.

## 5. Connections
- Combined by container runtimes
- Enforced by the kernel

