# 4. File Systems & Storage

### Intuition

Unix treats **everything as a file**:

- Files
- Directories
- Devices
- Sockets

The file system is how the OS **organizes reality**.

------

### Key Concepts

#### Files, Directories, Inodes

- Filename → pointer
- Inode → metadata + disk location
- Data → actual bytes

Deleting a file:

- Removes name
- Data stays until overwritten

------

#### Disk vs Memory

- Disk → persistent, slow
- Memory → temporary, fast

The OS constantly balances between them.

------

#### Buffers & Caches

Writes often:

- Go to memory first
- Reach disk later

This improves speed but risks data loss on crashes.

------

#### Permissions

Each file has:

- Owner
- Group
- Others

Permissions control **who can read, write, execute**.

------

### Mental Model

> Files are not objects — they are **agreements enforced by the OS**.