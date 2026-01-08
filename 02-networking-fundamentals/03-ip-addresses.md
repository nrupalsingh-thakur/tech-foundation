## 03 — IP Addresses (Finding the Right Machine)

### Why IP Exists

Packets need a destination.

Routers don’t know:
- your app
- your user
- your data meaning

They only know:
> “Where should this packet go next?”

---

### Mental Model

IP address = **street address**

Examples:
- `192.168.1.15`
- `10.0.0.2`
- `8.8.8.8`

Routers do one thing:
look at destination IP
forward packet closer to it

They do not care what’s inside.
