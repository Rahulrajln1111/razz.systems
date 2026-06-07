# RazzSec Lab

Personal CTF writeups, Linux notes, reversing notes, binary exploitation notes, web security notes, and security projects.

This site is based on [Fuwari](https://github.com/saicaca/fuwari), an Astro static blog template.

## Local Setup

```shell
pnpm install
pnpm dev
```

The dev server runs at `http://localhost:4321`.

## Add A New Writeup

```shell
pnpm new-post ctf-writeups/challenge-name.md
```

Then edit the generated file in `src/content/posts/`.

Use categories like:

- `CTF Writeups`
- `Linux`
- `Reverse Engineering`
- `Binary Exploitation`
- `Web Security`
- `Forensics`
- `Crypto`
- `Projects`
- `Notes`

Use tags like:

- `pwn`
- `rev`
- `linux`
- `gdb`
- `pwndbg`
- `ghidra`
- `burpsuite`
- `nmap`
- `pwntools`
- `htb`
- `tryhackme`
- `picoctf`

## Customize Your Identity

Edit these files:

- `src/config.ts` for site title, profile, navbar, social links, and banner
- `src/content/spec/about.md` for the About page
- `astro.config.mjs` for your final deployment URL

Replace remaining placeholder links like `your-linkedin` and `you@example.com`.

## Custom Domain

The production site URL is configured as:

```text
https://razz.systems/
```

If deploying with GitHub Pages, keep `public/CNAME`:

```text
razz.systems
```

At Name.com DNS, use these records for GitHub Pages:

```text
Type   Host   Answer
A      @      185.199.108.153
A      @      185.199.109.153
A      @      185.199.110.153
A      @      185.199.111.153
AAAA   @      2606:50c0:8000::153
AAAA   @      2606:50c0:8001::153
AAAA   @      2606:50c0:8002::153
AAAA   @      2606:50c0:8003::153
CNAME  www    Rahulrajln1111.github.io
```

In GitHub, also go to the repository **Settings -> Pages**, set the custom domain to `razz.systems`, save it, wait for DNS checks, then enable **Enforce HTTPS**.

If deploying with Vercel instead, add `razz.systems` in the Vercel project domains screen and use the DNS records Vercel gives you. Do not mix Vercel DNS records with GitHub Pages records.

## Build

```shell
pnpm build
```

The production output is written to `dist/`.
