---
title: Dell Vostro 3671 Build
description: A refurbished Dell Vostro 3671 office PC from Shopee (₱12,999) — my first desktop, upgraded one part at a time.
date: 2026-10-10
status: In Progress
tech: [PC Building, Intel, NVIDIA, DDR4, SATA SSD]
# pin: true
# image:
#   path: /assets/img/projects/dell-vostro-3671.jpg
#   alt: The Dell Vostro 3671 on my desk
---

<!--
  How to update this page whenever you upgrade:

  1. Add a new entry at the top of "Upgrade Log" (date, what changed, cost).
  2. Update the "Current Specs" table so it always reflects today.
  3. Tick the box of anything finished in "Planned Upgrades".
  4. Commit and push — the "Recently Updated" panel and the Projects list
     pick up the change automatically (the date comes from git).
-->

## Overview

My first PC I actually own. It started life as a boring office machine — a refurbished
Dell Vostro 3671 sold on Shopee for ₱12,999 — and it is slowly becoming a real
workstation for school, coding, and light gaming, one cheap upgrade at a time.

## Current Specs

| Component | Now | Notes |
|:--|:--|:--|
| CPU | Intel Core i7-9700 | 8 cores / 8 threads — already the top chip for this socket, no CPU upgrade path |
| RAM | 8 GB DDR4 | Single stick, 2666 MHz |
| Storage | 240 GB SATA SSD (boot) + 480 GB SATA SSD | Second drive added 2026-10-23 |
| GPU | GeForce GT 730 2 GB | Low-profile, slot-powered — current display output (UHD 630 iGPU as backup) |
| Case / PSU | Dell Vostro 3671 SFF | Proprietary ~290 W PSU (check the label on yours) |

## Desk Setup

| Peripheral | Now |
|:--|:--|
| Keyboard | Mechanical keyboard |
| Monitor | 15.6" external monitor |

## Purchase & Context

- **Where:** Shopee, refurbished office stock
- **Price:** ₱12,999
- **Why this machine:** a real quad-core-plus desktop with a decent upgrade path,
  at a price a student budget can survive

## Upgrade Log

### 2026-10-23 — Storage upgrade

- Added a **480 GB SATA SSD** — ₱3,500
- More room for games, projects, and files without touching the boot drive

### 2026-10-10 — Baseline (as purchased)

- Intel Core i7-9700, 8 GB DDR4, 240 GB SATA SSD, GT 730 2 GB
- Clean install, drivers updated, office dust blown out

## Planned Upgrades

- [ ] **RAM 8 → 16 GB** — add a matching DDR4-2666 stick (~₱1k, biggest cheap win)
- [ ] **GPU** — low-profile, slot-powered card that fits the SFF case and stock PSU
      (e.g. GTX 1650 LP / RTX 3050 6 GB LP class — verify PSU wattage first)
- [x] **Storage** — added a 480 GB SATA SSD (~₱3,500); expand to 1 TB when it fills up
- [ ] **Cooling & maintenance** — new thermal paste, maybe a quieter case fan

## Notes & Lessons

- The SFF case only accepts **half-height (low-profile)** cards, and the stock PSU
  has no PCIe power cables — slot-powered cards only.
- The i7-9700 is the top of its platform; the realistic gains are RAM, GPU, and storage.
- The i7-9700 includes Intel UHD 630 integrated graphics — a free backup if the
  GT 730 ever acts up, and one less thing to worry about during a GPU swap.
- Adding a SATA SSD was the easiest upgrade so far — no clearance or power-draw
  concerns, just a spare SATA data and power cable.

## Benchmarks

| Test | Baseline | After upgrades |
|:--|:--|:--|
| Cinebench R23 multi | — | — |
| Boot to desktop | — | — |
| Favorite game @ settings | — | — |
