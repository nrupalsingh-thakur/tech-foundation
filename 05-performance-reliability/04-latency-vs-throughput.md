# Latency vs Throughput

## 1. Why this matters
Many systems optimize the wrong thing.

## 2. Core idea
- Latency = time for one request
- Throughput = requests per second

You can improve one and hurt the other.

## 3. Mental model
Highway analogy:
- Latency → time for one car
- Throughput → cars per hour

## 4. Diagram

    Low latency, low throughput:
    |car|        |car|

    High throughput, higher latency:
    |car|car|car|car|car|

## 5. Real-world example
- Batching increases throughput
- Queues increase latency

## 6. Connections
- Networking (Level 2)
- Distributed systems later

