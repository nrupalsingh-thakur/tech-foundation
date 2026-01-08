## 11 — How DNS Lookup Works

### Flow

App

|

v

OS resolver

|

v

DNS servers

|

v

IP address

Steps:
1. App asks OS
2. OS checks cache
3. If missing, asks DNS
4. Gets IP
5. Caches result
6. Returns IP

Only then does networking begin.
