## 10. Linux Boot & Services

The purpose of the boot process is simple:

> Turn powered-off hardware into a usable operating system.

### High-Level Boot Flow

Power On
↓
BIOS / UEFI
↓
Bootloader (GRUB)
↓
Linux Kernel
↓
systemd (init)
↓
Services + Login

### Boot Process (Intuitive View)

- **BIOS / UEFI**
  - Firmware on the motherboard
  - Finds where the OS is stored
  - Loads the bootloader

- **Bootloader (GRUB)**
  - Chooses which OS or kernel to boot
  - Loads the Linux kernel into memory

- **Linux Kernel**
  - Core of the operating system
  - Initializes:
    - CPU
    - Memory
    - Devices
  - Does **not** manage applications directly

- **systemd (init)**
  - First userspace process
  - Always has **PID 1**
  - Parent of all other processes

---

### systemd (Init System)

`systemd` is the system manager.

Its responsibilities:
- Start services
- Stop services
- Restart crashed services
- Handle service dependencies

Example dependency logic:
Network
↓
Docker
↓
Web Application

systemd ensures things start in the correct order.

---

### Services vs Processes

**Process**
- A running program
- Exists in memory
- Has:
  - PID
  - Memory space
  - CPU time

Example:
python app.py

**Service**
- A managed, long-running process
- Supervised by systemd
- Can automatically restart

Examples:
sshd
nginx
docker

Relationship:
systemd (PID 1)
├── sshd (service)
├── nginx (service)
├── docker (service)
└── user processes

> A service is a process with supervision and rules.
