# 🦉 OConns

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-Security-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0-cyan?style=flat-square"/>
</p>

> **OConns** — part of the OwlSec Toolkit.

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OConns shows every network connection on a Linux machine, similar to ss -p or lsof. It reads /proc/net directly, decodes IPv4 and IPv6 sockets, and maps each one to the process that owns it. Its exposure audit flags risky listeners and suspicious outbound connections as graded findings.

---

## ✨ Features

- Reads /proc/net/{tcp,tcp6,udp,udp6}: addresses, states, tx/rx queues, UID and inode
- Maps every socket to its owning process (inode → PID → name)
- Listeners view, TCP state summary, top remote peers and per-port filter
- Live monitor with configurable duration and refresh interval
- Exposure audit: world-reachable listeners, plaintext service ports, rare ephemeral listeners, fan-out and suspicious ports
- Reports in TXT / JSON / Markdown / CSV / SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OConns                                     # interactive menu
./OConns --listen
./OConns --audit
./OConns --port 443
./OConns --monitor -t 60 --interval 2
```

Run `./OConns --help` for the full list of options.

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
