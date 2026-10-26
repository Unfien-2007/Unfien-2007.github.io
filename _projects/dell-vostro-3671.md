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
| RAM | 16 GB DDR4 | 2 × 8 GB, 2666 MHz — second stick added 2026-10-26 for ₱2,000 |
| Storage | 240 GB SATA SSD (boot) + 480 GB SATA SSD | Second drive added 2026-10-23 (bought Dec 2025) |
| GPU | GeForce GT 730 2 GB | Slot-powered — current display output (UHD 630 iGPU as backup) |
| Cooling | Stock CPU cooler + 92 mm PWM rear exhaust | Fan added 2026-10-16 |
| Case / PSU | Dell Vostro 3671 micro tower | Proprietary ~290 W PSU (check the label on yours) |

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

## Total Cost

| Item | Cost |
|:--|--:|
| Dell Vostro 3671 (refurbished, Shopee) | ₱12,999 |
| 480 GB SATA SSD (bought Dec 2025) | ₱3,500 |
| 8 GB DDR4-2666 RAM | ₱2,000 |
| 92 mm PWM fan + SATA-to-PWM adapters | not recorded |
| **Total (known)** | **₱18,499** |

Peripherals (mechanical keyboard, 15.6" external monitor) are not included in
this total because I don't have their prices on hand.

## Upgrade Log

### 2026-10-26 — RAM upgrade

- Added another **8 GB DDR4-2666 stick** — ₱2,000
- Now running **16 GB in dual channel**, which finally gives enough headroom for
  VMs, a few browser windows, and code editor + server running at the same time

### 2026-10-23 — Storage upgrade

- Added a **480 GB SATA SSD** — ₱3,500
- The drive was bought back in **December 2025** and finally made it into the build
- More room for games, projects, and files without touching the boot drive

### 2026-10-16 — Cooling upgrade

- Added a **92 mm PWM fan** as a rear exhaust
- Connected with **SATA-to-PWM adapters** (SATA power, PWM control)
- Goal: better airflow out of the micro tower and lower temperatures

### 2026-10-10 — Baseline (as purchased)

- Intel Core i7-9700, 8 GB DDR4, 240 GB SATA SSD, GT 730 2 GB
- Clean install, drivers updated, office dust blown out

## Planned Upgrades

- [x] **RAM 8 → 16 GB** — added a matching DDR4-2666 stick (₱2,000, 2026-10-26)
- [ ] **GPU** — slot-powered card that works with the stock PSU
      (e.g. GTX 1650 / RTX 3050 6 GB class — verify wattage and connectors first)
- [x] **Storage** — added a 480 GB SATA SSD (~₱3,500); expand to 1 TB when it fills up
- [x] **Cooling** — added a 92 mm PWM rear exhaust fan (2026-10-16)
- [ ] **Maintenance** — new thermal paste, and maybe quieter fans

## Notes & Lessons

- The micro tower has full-height expansion slots, but the stock PSU has no PCIe
  power cables — slot-powered cards only unless the PSU is replaced.
- The i7-9700 is the top of its platform; the realistic gains are RAM, GPU, and storage.
- The i7-9700 includes Intel UHD 630 integrated graphics — a free backup if the
  GT 730 ever acts up, and one less thing to worry about during a GPU swap.
- Adding a SATA SSD was the easiest upgrade so far — no clearance or power-draw
  concerns, just a spare SATA data and power cable.
- A 92 mm PWM rear exhaust is an easy cooling win in this case, and SATA-to-PWM
  adapters keep the install simple.
