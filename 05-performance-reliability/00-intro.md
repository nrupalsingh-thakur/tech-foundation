# Level 5 — Performance & Reliability

## 1. What problem does this level solve?
Systems that:
- Are “up” but slow
- Randomly fail under load
- Work in dev but not in prod

## 2. Core idea
Every system is limited by:
- CPU
- Memory
- I/O
- Network

Performance problems are about **which limit you hit first**.

## 3. Mental model
A system is like a factory:
- Too few workers → CPU bottleneck
- Too little workspace → memory bottleneck
- Slow conveyor belts → I/O bottleneck

## 4. Diagram — system pressure

        Requests
           │
           ▼
     ┌────────────┐
     │ Application│
     └─────▲──────┘
           │
   ┌───────┼────────┐
   │ CPU   │ Memory │ I/O
   └───────┴────────┴───► Bottleneck appears

## 5. Connections
- Built on OS scheduling & memory
- Explains container and cloud failures

