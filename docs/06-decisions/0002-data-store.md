# ADR 0002: Data store for Elias v0.1 (SQLite vs JSON files)

**Status:** Accepted  
**Date:** 2026-02-24

## Context
Elias v0.1 needs a local-first data store for:
- household state (animals, chores, routines)
- event history (what happened, when)
- notification audit logs

Key priorities:
- Reliability (avoid partial writes and inconsistent state)
- Easy queries for dashboards/reminders
- Simple backup/restore
- Low setup friction

Options considered:
- SQLite (single local database file)
- JSON files (one or many files holding state/logs)

## Decision
For v0.1, Elias will use **SQLite** as the primary local data store.

## Consequences
### Positive
- Reliable writes (transactions)
- Easy querying (“what’s due?”, “last fed?”)
- Simple backups (copy one file)
- Smooth upgrade path as features expand

### Negative / Tradeoffs
- Requires basic schema management (tables/migrations)
- Slightly more structure upfront vs JSON

## Alternatives Considered
- JSON files: rejected due to higher risk of inconsistent state/log fragmentation and harder long-term querying.
