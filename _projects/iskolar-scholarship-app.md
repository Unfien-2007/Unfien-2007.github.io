---
title: Iskolar — Scholarship Finder & Application Tracker
description: >-
  My Java OOP final exam project — a scholarship finder I'm building with AI
  assistance to learn Java 21, JavaFX, and SQLite. A work in progress, and so
  is my understanding of it.
date: 2026-10-31
status: In Progress
tech: [Java 21, JavaFX, SQLite, Maven, JUnit 5, Spring Boot, Render, Neon]
repo: https://github.com/Unfien-2007/iskolarsql
pin: true
---

<!--
  How to keep this page honest and easy to update:

  1. "What I'm still learning" is a checklist. When I can explain an item in my
     own words, tick it and add a short note under "Notes as I learn".
  2. Keep the Overview plain — this is a learning project, not a finished product.
  3. Change `status` to Completed only when the app actually works end to end.
  4. Commit and push; the Projects list picks the change up automatically.
-->

## Overview

Iskolar is a desktop app for Filipino students: find scholarships, see which ones
fit your profile, and track applications on a kanban board. I built it as the final
exam project for my Java OOP course (2nd year, 1st semester). It is still in
progress — some flows work end to end, others are rough or unfinished.

I built it with AI assistance, and I'm saying so on purpose. The point of the project
is learning, not shipping: I go through each phase, read what the code actually does,
and write down what I understand and what I don't. That list is further down. Anything
on this page is something I'm willing to be asked about.

## What the app does

What is built so far:

- **Discovery grid** — scholarship cards with filters by program, year, provider,
  and location
- **Matching engine** — two-stage matching: hard eligibility gates first, then a
  weighted score with a grace band for borderline grades
- **Application tracker** — kanban board with validated stage moves
- **Profile wizard** — four-step form with progressive saves, GWA conversion, and a
  document list
- **Admin portal** — scholarship catalog and eligibility-rule editor
- **Accounts** — login and registration with BCrypt-hashed passwords

## Companion API

The desktop app doesn't work alone: a small **Spring Boot** service (`server/`) serves
the scholarship catalog and handles account auth with JWT. It runs on **Render** (free
tier, Docker) with a **Neon** Postgres database. The app polls it for catalog updates
and keeps a cached copy so matching still works offline.

Deployed endpoints: health check, register/login, password reset, catalog snapshot and
version.

## Stack

| Layer | Used for |
|---|---|
| Java 21 | records, switch expressions, pattern matching |
| JavaFX 21 (FXML + CSS) | screens, navigation, light/dark theme |
| Maven | build and `javafx:run` |
| SQLite + JDBC/HikariCP | local database and pooled connections |
| JUnit 5 | tests, mainly around the matching engine |
| Spring Boot | companion API — catalog and auth endpoints |
| Render + Neon | API hosting (Docker, free tier) and Postgres database |
| jBCrypt | password hashing |

## How I'm learning with it

The app was built in phases, and I review each phase before starting the next:

1. Database schema and seed data
2. Domain model and database access layer (DAOs)
3. Matching engine and its tests
4. App shell, navigation, themes, and auth
5. Screens — login, discovery, profile wizard, kanban, comparison, admin

AI assistance gets the code written faster than I would alone. My job is the slower
part: read it, run it, break it, and be able to explain it. When I can't, it goes on
the list below.

## What I'm still learning

Honest list. Tick an item when I can explain it without looking it up, then add a
short note under "Notes as I learn":

- [ ] How the DAO layer builds and runs its SQL (prepared statements)
- [ ] Why the matching engine uses these specific weights (35/30/20/15)
- [ ] What HikariCP does that a plain JDBC connection doesn't
- [ ] How an FXML controller reaches a service and a model
- [ ] How the companion `server/` API (Spring Boot + JWT) fits into the app

## Notes as I learn

<!-- Add a dated line whenever an item is ticked off, for example:
- **2026-11-14** — HikariCP: keeps a pool of open connections so every screen
  doesn't pay the cost of opening a new one. -->

Nothing written yet — this grows as I work through the codebase.
