## 12 — DNS Caching (The Source of Many Bugs)

### Why Caching Exists

DNS lookups are slow.
Caching saves time.

---

### Why It Breaks Things

Caches exist at:
- app level
- OS level
- router level
- ISP level

Result:
- different machines see different IPs
- changes propagate slowly

This explains:
> “It works on my laptop but not in prod”
