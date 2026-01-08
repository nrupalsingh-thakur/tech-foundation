## 02 — Packets (Why Data Is Chopped Up)

### The Problem

You want to send a large message.
The network is unreliable.

Links can:
- fail
- drop data
- get congested

Sending everything at once would be fragile.

---

### The Solution: Packets

The OS breaks data into **small pieces**.

**Mental model:**  
Shipping a couch as many boxes, not one giant crate.

Large message

|

v

[packet][packet][packet][packet]

Each packet includes:
- source IP
- destination IP
- sequence info
- a slice of data

Packets may:
- arrive out of order
- arrive late
- never arrive

This is **expected behavior**, not a bug.
