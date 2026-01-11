# I/O Bottlenecks

## 1. What problem does this solve?
Low CPU usage but slow performance.

## 2. Core idea
I/O bottlenecks happen when:
- Disk is slow
- Network is slow
- Processes wait instead of running

## 3. Mental model
I/O is waiting in line:
- CPU asks for data
- CPU waits doing nothing

## 4. Diagram — I/O wait

    CPU ──request──▶ Disk
     │               │
     └────── wait ◀──┘

## 5. Linux symptoms
- High iowait
- Low CPU usage
- Slow response times

## 6. Connections
- Filesystems (Level 1)
- Networking (Level 2)

