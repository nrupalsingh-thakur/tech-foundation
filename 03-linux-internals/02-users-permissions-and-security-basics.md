## 11. Users, Permissions & Security Basics

Linux security is built on a simple idea:

> Every action is performed by a user, and every resource has rules.

---

### UID & GID

**UID (User ID)**
- Numerical identity of a user
- Example:
  - `0` → root
  - `1000+` → normal users

**GID (Group ID)**
- Numerical identity of a group
- Used to share access between users

Linux uses numbers internally because they are fast and unambiguous.

---

### File Permissions

Each file has three permission scopes:

Owner | Group | Others

Each scope can have:
- `r` → read
- `w` → write
- `x` → execute

Example:
-rwxr-x---

Meaning:
Owner: read, write, execute
Group: read, execute
Others: no access

Permission check order:
1. Owner
2. Group
3. Others

Only one level applies.

---

### Capabilities (High Level)

Traditionally:
- `root` had unlimited power
- Non-root had very limited power

Problem:
> Root access is too dangerous.

**Capabilities** split root power into smaller permissions.

Examples:
- Bind to low ports
- Manage network settings
- Perform system administration tasks

This allows:
> Giving only the minimum power required

Result:
- Better security
- Smaller attack surface

