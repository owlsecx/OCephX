# 🦉 OCephX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OCephX** — Ceph Storage Cluster Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OCephX is an offline, read-only auditor for Ceph storage cluster configuration, parsing ceph.conf, keyrings and the text/JSON output of ceph auth, config and pool commands. It reviews cephx authentication, msgr2 secure messaging, keyring capabilities and permissions, RGW and CephFS exposure, the dashboard and data-protection settings. Secrets are masked everywhere, findings map to CWE and MITRE ATT&CK, and results roll up into an A+…F grade with hardened templates.

---

## ✨ Features

- Parses ceph.conf, keyrings and ceph auth/config/pool exports (text + JSON)
- cephx checks: auth_*_required, signatures, global_id reclaim (CVE-2021-20288), TTLs
- msgr2 secure-mode and legacy msgr1 detection
- Keyring capability and world/group-readable permission analysis
- RGW TLS/ACL, dashboard hardening and pool size/min_size data-protection checks
- Secrets masked; hardened templates and export TXT/MD/JSON/CSV/SARIF

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCephX --scan
./OCephX /etc/ceph/ceph.conf --format json -o report.json --fail-on high
./OCephX --root /mnt/image --scan
./OCephX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
