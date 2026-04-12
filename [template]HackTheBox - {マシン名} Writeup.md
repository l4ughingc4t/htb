+++
title = "HackTheBox - [マシン名] Writeup"
date = "YYYY-MM-DD"
description = "[概要を1行で]"
tags = ["HackTheBox", "CTF", "[OS]", "[脆弱性名]", "[使用ツール]", "[難易度]"]
categories = ["HackTheBox"]
toc = true
draft = false
+++

## Machine Info

| Field | Details |
|-------|---------|
| Machine | [Machine Name] |
| OS | [OS Name] |

---

## Reconnaissance

### Nmap Scan

```bash
nmap -sV [IP]
```

```text
[Nmap output here]
```

---

## [Initial Access Method (e.g. FTP Access / Web Fuzzing)]

```bash
[command]
```

```text
[output]
```

---

## Payload Generation

```bash
[msfvenom or other payload command]
```

---

## Upload / Delivery

```bash
[command]
```

---

## Trigger

```bash
[command to trigger the payload]
```

---

## Listener

```bash
[nc or metasploit listener command]
```

```text
[connection output]
```

---

## Foothold

```bash
whoami
```

```text
[current user]
```

---

## System Info

```bash
[systeminfo or uname -a]
```

```text
[output]
```

---

## Post Exploitation

```bash
[enumeration commands]
```

---

## Results

- [Exploit candidate 1]
- [Exploit candidate 2]
- [Exploit candidate 3]

---

## Privilege Escalation

```bash
[privesc exploit command]
```

---

## [SYSTEM / Root] Shell

```bash
[whoami / getuid]
```

```text
[NT AUTHORITY\SYSTEM or root]
```

---

## Flags

### User

```bash
[command to read user.txt]
```

### Root

```bash
[command to read root.txt]
```

---

## Summary

[Initial access method] → [foothold] → [privesc method] → [SYSTEM/root]
