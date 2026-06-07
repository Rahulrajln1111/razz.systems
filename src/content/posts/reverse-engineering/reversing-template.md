---
title: "Reverse Engineering Template"
published: 2026-06-07
description: "A reusable structure for Ghidra, strings, patching, and control-flow writeups."
image: ""
tags: ["reverse-engineering", "ghidra", "strings", "debugging"]
category: "Reverse Engineering"
draft: false
lang: ""
---

## Challenge Info

- **Platform:** Replace
- **File type:** ELF/PE/APK/etc.
- **Goal:** Recover password, flag, algorithm, or hidden behavior

## First Look

```shellsession
$ file ./chall
$ strings ./chall | less
$ ltrace ./chall
```

## Static Analysis

Open the binary in Ghidra and rename important functions/variables as you understand them.

Track:

- input checks
- hardcoded constants
- encoding/encryption loops
- suspicious branches

## Dynamic Analysis

```shellsession
$ gdb ./chall
```

Useful breakpoints:

```text
break main
break strcmp
break puts
run
```

## Solution

Explain the condition needed to reach the success branch.

```python
# solver.py
print("replace_with_solution")
```

## Lessons Learned

- What made the binary confusing?
- Which tool gave the key insight?
