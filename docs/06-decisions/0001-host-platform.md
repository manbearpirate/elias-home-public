# ADR 0001: Host platform for Elias Core (low-power home server vs always-on PC)

**Status:** Accepted  
**Date:** 2026-02-24

## Context
Elias Core needs a reliable “always-on” host for early versions.
Priorities include:
- Stability and predictable behavior
- Low power draw
- Minimal maintenance overhead
- Clear upgrade path later without rework

## Decision
For early versions (v0.1), Elias Core will run on a **low-power home server** rather than a daily-use always-on PC.

Upgrading/migrating later is explicitly allowed, but not a near-term task. The focus is shipping v0.1 functionality first.

## Consequences

### Positive
- More reliable always-on behavior with fewer disruptive updates/reboots
- Lower power use
- Separates household services from daily-use computing

### Negative / Tradeoffs
- Requires light home-server maintenance practices (backups, monitoring)
- Performance is lower than a full PC (fine for v0.x)

## Alternatives Considered
- Always-on PC (rejected for early versions due to update/reboot churn and higher fragility)
- NAS host (deferred)
- Cloud host (deferred/rejected early due to privacy/complexity)
