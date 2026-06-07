---
title: "Start Here: RazzSec Lab"
published: 2026-06-07
description: "How this site is organized and how to add new CTF writeups or projects."
image: ""
tags: ["site", "ctf", "writeups", "projects"]
category: "Notes"
draft: false
lang: ""
---

This site is organized as a personal CTF lab and security notebook.

## Main Sections

- **CTF Writeups:** full challenge walkthroughs
- **Linux:** enumeration, privilege escalation, shell workflow
- **Reverse Engineering:** Ghidra, debugging, binary analysis
- **Binary Exploitation:** stack, ROP, format strings, pwntools
- **Web Security:** Burp, auth bugs, injection, file upload issues
- **Projects:** tools, scripts, exploit templates, and security experiments

## Add A New Writeup

Create a new Markdown file under `src/content/posts/`.

```shellsession
$ pnpm new-post ctf-writeups/my-new-writeup.md
```

Then set the frontmatter:

```yaml
title: "Challenge Name - Platform"
published: 2026-06-07
description: "One sentence summary."
tags: ["pwn", "gdb", "pwntools"]
category: "CTF Writeups"
draft: false
```

## Recommended Writeup Structure

1. Challenge info
2. Recon
3. Analysis
4. Exploit or solution
5. Flag/result
6. Lessons learned
