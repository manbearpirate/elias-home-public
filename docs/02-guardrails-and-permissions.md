# Elias Architecture (Public, High Level)

This document describes the high-level architecture for Elias Home. Detailed implementation specifics are intentionally kept private.

---

## Goals
- Reduce household cognitive load (chores, calendar visibility, reminders)
- Improve consistency for animal care routines
- Keep the system calm, simple, and reliable under stress
- Preserve privacy and data ownership where feasible

---

## Components

### 1) Kitchen-Friendly UI
- A tablet-friendly “Today View” dashboard
- Quick visibility into:
  - animal status
  - chores due
  - calendar (read-only)
  - alerts/reminders

### 2) Elias Core Service
- Stores household “state” (what’s true right now)
- Stores event “history” (what happened and when)
- Evaluates reminder rules (quiet hours, snooze behavior, etc.)
- Produces notifications and dashboard data

### 3) Local Data Store
- SQLite database for:
  - animal status + history
  - chores + history
  - notification audit logs

### 4) Integrations (Phased)
- Calendar (read-only early, write later)
- Notifications (push and/or dashboard)
- Optional voice interface (read-only first)
- Optional LLM support behind strict guardrails

---

## Design Pattern: State + Event Log
Elias uses two kinds of data:
- **Current state** for fast dashboard reads
- **Event logs** for auditability and history (“when was the last feeding?”)

---

## Safety Model (Guardrails)
- Read-only by default
- Actions must be allowlisted (Action Catalog)
- Sensitive actions require explicit confirmation
- Quiet hours respected
- Audit logging for notifications/actions

---

## What’s intentionally not included here
- Household network details
- Device identifiers or locations
- Authentication secrets or tokens
