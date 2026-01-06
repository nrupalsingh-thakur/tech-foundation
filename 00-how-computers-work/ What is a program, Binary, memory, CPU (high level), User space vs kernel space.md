Nice—Day 1 is exactly the right time to build **strong mental models**. If these click now, *everything* in OS later will feel way less scary. I’ll keep it **light, concrete, and visual**.

------

# LEVEL 0 — How Computers Think

*(Mental models, not heavy theory)*

------

## 1️⃣ What is a **Program**?

### Simple definition

A **program** is a **set of instructions** that tells the computer **what to do, step by step**.

That’s it. No magic.

------

### Human analogy

Imagine a robot that can only follow instructions **exactly as written**.

**Program = instruction list**

```text
1. Take bread
2. Put peanut butter on bread
3. Put jelly on bread
4. Close sandwich
```

If you forget a step → robot fails.
Computers are the same, just way faster and more literal.

------

### Computer example

This tiny program adds two numbers:

```python
a = 5
b = 3
print(a + b)
```

What the computer understands:

- Store `5`
- Store `3`
- Add them
- Show result

📌 **Key idea**:
A program is **data + instructions**.

------

### Important mental model

> A computer does **nothing by itself**.
> Everything happens because a program tells it to.

------

## 2️⃣ Binary, Memory, CPU (High-Level)

This is the **core triangle** of computing.

------

## 🔢 Binary (Why 0 and 1?)

Computers are made of **electronic switches**.

- ON → `1`
- OFF → `0`

They can’t naturally understand:

- letters
- images
- videos
- music

So everything becomes **0s and 1s**.

------

### Example

Letter **A** = `65`
`65` in binary = `01000001`

So when you see:

```text
A
```

The computer sees:

```text
01000001
```

📌 **Key idea**:

> Everything is binary underneath — text, images, programs, OS, everything.

------

## 🧠 Memory (RAM)

### What memory is

**Memory = temporary storage** where the computer keeps:

- running programs
- data they are using right now

Think of memory like a **desk**.

------

### Analogy

- **Hard disk** → cupboard (slow, permanent)
- **Memory (RAM)** → desk (fast, temporary)

If the desk is small:

- you can work on fewer things at once

------

### Example

When you open:

- Chrome
- Music player
- VS Code

They all sit in **memory**.

When power goes off → memory is **wiped**.

📌 **Key idea**:

> Programs must be in memory to run.

------

## ⚙️ CPU (The Brain)

### What CPU does

The **CPU executes instructions**.

It does this loop *billions of times per second*:

```text
1. Fetch instruction from memory
2. Decode instruction
3. Execute instruction
```

This is called the **Fetch–Decode–Execute cycle**.

------

### Example

Instruction:

```text
ADD 5, 3
```

CPU:

- Fetches it
- Understands "ADD"
- Performs addition
- Stores result

📌 **Key idea**:

> CPU doesn’t store much — it **processes**.

------

## 🔺 Big Picture Diagram

```
+-------------+
|   Program   |
+-------------+
       |
       v
+-------------+        +-------------+
|   Memory    | <----> |     CPU     |
|   (RAM)     |        | (Executes)  |
+-------------+        +-------------+
       |
       v
+-------------+
|   Binary    |
|   (0s & 1s) |
+-------------+
```

------

## 3️⃣ User Space vs Kernel Space

This is **VERY IMPORTANT** for OS later.

------

## 🧍 User Space

### What it is

Where **normal programs** run:

- Browser
- Games
- Text editor
- Your code

They:

- **cannot** directly control hardware
- **cannot** access memory freely

This is for **safety**.

------

### Example

Your program **cannot**:

- access someone else’s memory
- shut down the CPU
- control the disk directly

If it could → chaos 😅

------

## 👑 Kernel Space

### What it is

Where the **Operating System kernel** runs.

Kernel can:

- talk to hardware
- manage memory
- schedule CPU
- control files
- handle devices

Kernel = **boss mode**

------

### How user programs do powerful things

They **ask** the kernel.

This is called a **system call**.

------

### Example: Printing text

```python
print("Hello")
```

What *really* happens:

```
Your Program (User Space)
        |
        | system call
        v
Operating System Kernel
        |
        v
Screen Hardware
```

Your program never touches hardware directly.

📌 **Key idea**:

> User space asks. Kernel decides.

------

## 🧠 Why this separation exists

1. **Security** – one bad app can’t destroy the system
2. **Stability** – crashes don’t kill the OS
3. **Control** – OS manages resources fairly

------

## 🧩 Final Mental Model (This is gold)

```
[ Your Program ]
     |
     |  system calls
     v
[ Operating System (Kernel) ]
     |
     v
[ Hardware (CPU, Memory, Disk, Screen) ]
```

If you remember **only this**, you’re ahead of many learners.

------

## 📚 Good Beginner Resources (Safe & Clear)

### 🔹 Reading (Beginner-friendly)

- *“Operating Systems: Three Easy Pieces”*
  👉 Read **only the intro chapters** for now

------

