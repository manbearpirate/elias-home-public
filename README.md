![Project Status](https://img.shields.io/badge/status-active%20development-blue)
![Architecture](https://img.shields.io/badge/architecture-documented-success)
![License](https://img.shields.io/badge/license-MIT-green)

---

# Elias Home (Public)

Elias is our family’s **home hub** project — a gentle, local-first assistant designed to reduce mental load and help everyday life run smoothly.

Think: **kitchen-friendly dashboard + reminders + animal-care tracking**, with later phases adding voice (“Hey Elias…”) and meal planning.

> **Core vibe:** helpful, calm, and reliable — not naggy, not creepy, not autonomous.

---

## What Elias Is

Elias is a **local-first household steward system** designed to reduce mental load and help keep a home running smoothly.

It began with simple goals:

- track rabbit care
- manage household chores
- provide a calm kitchen dashboard
- surface reminders without becoming noisy

Over time it is evolving into a broader system for:

- household routines
- operational visibility
- homestead stewardship
- long-term household memory

---

## Start Here (non-technical)
- **What it is:** a calm home dashboard + reminders system (local-first).
- **Why:** fewer missed chores/appointments + smoother routines.
- **Current focus:** v0.1 “System of Record” (track key household info reliably).

---

## What Elias Does (Roadmap)

### v0.1 — System of Record (current focus)
- Animal care tracking: status + history (feed/water/etc.)
- Chore tracking: what’s due + when it was last done
- Simple dashboard views (read-only first)

### v0.2 — Reminders + Notifications
- Reminders and notifications (with quiet hours + snooze)
- “Don’t spam us” rules + audit log

### v0.3 — Kitchen Hub MVP
- Tablet “Today View”:
  - animal status
  - chores due
  - calendar (read-only)
  - alerts

### v0.4+ — One-tap Logging + Routines
- Buttons like “Fed animals” / “Topped water”
- Routine cards (Movie Night / Bedtime / etc.)

### v0.7+ — Voice Read-Only
- “Hey Elias” → answers, status checks, reminders

### v2.0+ — Voice Actions (Controlled)
- **Allowlisted** actions only (Action Catalog)
- Confirmations + audit logging

### v3.0+ — Meal Planning + Inventory
- Inventory-lite first (pantry/fridge/freezer awareness)
- Waste reduction + smart suggestions
- Safety-first guidance for household + homestead contexts

---

## Guiding Principles (Guardrails)
- **Local-first** where possible (privacy + reliability)
- **Read-only by default**
- Actions must be **explicitly allowlisted**
- **Quiet hours** respected
- **Snooze > dismiss**
- Keep it family-friendly: simple UI, big text, low friction

---

## Architecture Snapshot

Elias is built around a few simple layers:

Users  
↓  
Elias Face (dashboard / tablet UI)  
↓  
Elias Core (household logic + reminders)  
↓  
Data Store (SQLite)  
↓  
Events & History

Later architecture expands to include:

- **Elias Brain** — infrastructure and monitoring
- **Tobias Sentinel** — observability layer
- **Codex** — long-term household knowledge

---

## Architecture (High Level)
This public repo intentionally stays high-level. Implementation details that could expose a household environment are kept private.

- **UI:** tablet-friendly dashboard (browser)
- **Core:** a small local service that stores household state and evaluates reminder rules
- **Data store:** SQLite (simple, reliable, easy backups)
- **Future:** optional voice + optional LLM support behind permissions

---

## Project Status

Elias is currently in **early active development**.

| Area | Status | Notes |
|-----|------|------|
| Architecture | Stable | Core system structure defined |
| Documentation | Strong | Architecture, roadmap, guardrails, ADRs |
| Elias Core | Scaffolded | Initial FastAPI service skeleton |
| Elias Face | Scaffolded | Dashboard UI placeholder |
| Infrastructure | Planned | Elias Brain Bronze Build defined |
| Data Model | Stable | SQLite schema and event model |
| Rabbit Tracking | Planned | First working feature target |
| Chore Tracking | Planned | Second working feature target |

Next milestone:

**Connect Elias Core → SQLite → Dashboard**

---

## Current Development Focus

The immediate goal is to produce a **minimal working household dashboard**.

Short-term milestones:

1. Connect Elias Core to the SQLite schema
2. Implement rabbit care API endpoints
3. Implement chore tracking endpoints
4. Connect Elias Face dashboard to live Core data

Once that works reliably, the project will move into reminder logic and routine support.

---

## Repo Map
- `docs/`
  - `01-architecture.md` — high-level architecture overview
  - `02-guardrails-and-permissions.md` — safety + permissions rules
  - `03-roadmap.md` — milestones and direction
  - `04-feature-matrix.md` — version-by-version feature matrix
  - `06-decisions/` — ADRs (decision records)

---

## Key Docs
- [Architecture](docs/01-architecture.md)
- [Guardrails & Permissions](docs/02-guardrails-and-permissions.md)
- [Roadmap](docs/03-roadmap.md)
- [Feature Matrix](docs/04-feature-matrix.md)
- [Decisions (ADRs)](docs/06-decisions/)

---

## Status
Active build. Early prototype phase (**v0.x**) with a focus on shipping **small, safe, real wins** before adding complexity.

---

## Why This Project Exists

Most smart-home systems optimize for gadgets.

Elias optimizes for **household calm**.

The idea is simple:

- fewer forgotten chores
- clearer rabbit care tracking
- a kitchen dashboard that answers “what’s going on today?”
- reminders that are helpful but not annoying
- a system that supports family life rather than interrupting it

Over time Elias may also support homestead stewardship through the Red Barn Initiative.

---

## How to Contribute
Open an Issue titled: **“I want Elias to…”** (one sentence is perfect).

---

## Inspiration

Elias draws inspiration from ideas like:

- calm technology
- local-first software
- homestead record keeping
- operational observability
- household dashboards

The long-term vision is a system that quietly supports daily life without becoming intrusive or complicated.

---

## For the Humans
Elias exists for one reason: **make home life easier** — fewer missed tasks, fewer “oh no we forgot,” and less stress when we’re already carrying a lot.

❤️
