---
title: "Web Security Notes Template"
published: 2026-06-07
description: "A reusable structure for web exploitation writeups."
image: ""
tags: ["web", "burpsuite", "idor", "injection", "ctf"]
category: "Web Security"
draft: false
lang: ""
---

## Target Summary

- **Platform:** Replace
- **Category:** Web
- **Bug class:** Replace

## Recon

Record routes, parameters, roles, cookies, headers, and interesting JavaScript.

```shellsession
$ feroxbuster -u http://target/ -w /path/to/wordlist.txt
```

## Vulnerability

Explain the root cause:

- missing authorization check
- unsafe query construction
- weak session handling
- file upload validation issue

## Exploitation

Show the key request or payload.

```http
GET /api/user/2 HTTP/1.1
Host: target
Cookie: session=replace
```

## Lessons Learned

- What signal led you to the bug?
- What should you test earlier next time?
