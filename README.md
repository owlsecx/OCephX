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

Offline Ceph storage cluster configuration auditor (cephx, msgr2, keyrings, RGW, CephFS, dashboard)

---

## ✨ Features

- Offline, read-only parsers: ceph.conf (INI with Ceph section precedence), keyrings, `ceph auth ls/export`, `ceph config dump` (text + JSON), `ceph config-key dump`, `ceph osd pool ls detail` / `ceph osd dump` (text + JSON), RGW bucket ACL exports and /etc/fstab CephFS mounts
- cephx — auth_*_required, signatures, global_id reclaim (CVE-2021-20288), ticket TTLs, auth debug
- msgr2 — ms_*_mode secure, msgr1 legacy, mon_host v1-only
- Keyrings — world/group readable, client.admin on non-admin hosts, broad caps (mon 'allow *', osd 'allow *' w/o pool), duplicated / malformed keys, bootstrap keys, inline keys
- RGW — TLS frontends, Keystone / LDAP transport, SSE-KMS testing keys, static SSE key, anonymous (AllUsers) ACLs
- Dashboard — SSL, password policy, lockout, JWT TTL, default / weak admin, Grafana / RGW TLS verification
- Data protection — size / min_size, pool delete guard, size-one pools, dm-crypt hints, scrub flags, checksums
- Secrets masked everywhere; --root offline image audits
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Self-test --demo, CI gates --fail-on / --min-severity

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OCephX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
