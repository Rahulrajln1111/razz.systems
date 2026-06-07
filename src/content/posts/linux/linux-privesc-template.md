---
title: "Linux Privilege Escalation Template"
published: 2026-06-07
description: "A reusable structure for Linux box writeups and privilege escalation notes."
image: ""
tags: ["linux", "privilege-escalation", "enumeration", "ctf"]
category: "Linux"
draft: false
lang: ""
---

## Target Summary

- **Platform:** Replace with HTB/TryHackMe/local lab
- **Difficulty:** Replace
- **Initial access:** Replace
- **Privilege escalation path:** Replace

## Enumeration

```shellsession
$ nmap -sC -sV -oN nmap.txt <target-ip>
```

Record exposed services, versions, and anything unusual.

## Initial Access

Explain the path clearly:

1. What service or page looked interesting?
2. What vulnerability or misconfiguration was present?
3. How did you get a shell?

```shellsession
$ nc -lvnp 4444
```

## Local Enumeration

```shellsession
$ id
$ sudo -l
$ find / -perm -4000 -type f 2>/dev/null
$ ss -tulpen
```

## Privilege Escalation

Describe the weak permission, vulnerable binary, cron job, credential leak, or kernel issue.

```shellsession
$ whoami
root
```

## Proof

```text
user.txt: replace
root.txt: replace
```

## Lessons Learned

- Add the command, concept, or trick worth remembering.
