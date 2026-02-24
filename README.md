# Elias Home (Public)

Elias is our family’s **home hub** project — a gentle, local-first assistant designed to reduce mental load and help everyday life run smoothly.

Think: **kitchen-friendly dashboard + reminders + animal-care tracking**, with later phases adding voice (“Hey Elias…”) and meal planning.

> **Core vibe:** helpful, calm, and reliable — not naggy, not creepy, not autonomous.

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

## Architecture (High Level)
This public repo intentionally stays high-level. Implementation details that could expose a household environment are kept private.

- **UI:** tablet-friendly dashboard (browser)
- **Core:** a small local service that stores household state and evaluates reminder rules
- **Data store:** SQLite (simple, reliable, easy backups)
- **Future:** optional voice + optional LLM support behind permissions

---

## Repo Map
- `docs/`
  - `01-architecture.md` — high-level architecture overview
  - `02-guardrails-and-permissions.md` — safety + permissions rules
  - `03-roadmap.md` — milestones and direction
  - `04-feature-matrix.md` — version-by-version feature matrix
  - `06-decisions/` — ADRs (decision records)

---

## Status
Active build. Early prototype phase (**v0.x**) with a focus on shipping **small, safe, real wins** before adding complexity.

---

## For the Humans
Elias exists for one reason: **make home life easier** — fewer missed tasks, fewer “oh no we forgot,” and less stress when we’re already carrying a lot.

❤️
