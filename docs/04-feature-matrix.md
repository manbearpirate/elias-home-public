# Elias Feature Matrix (v0.1.0 → v3.0.0)

Legend:
- Risk: Low / Med / High
- Guardrails: controls that prevent “oops” moments
- Dependencies: what must exist first

| Version | Theme | Features (What it does) | Dependencies | Risk | Guardrails | Done When |
|---|---|---|---|---|---|---|
| v0.1.0 | System of Record | Rabbit feed/water log; chore log; simple notes; manual “status check” screen | Simple datastore (file/db); basic UI | Low | No device control; no purchases; no calendar writes | You can log + view rabbit status & chores reliably |
| v0.2.0 | Reminders + Notifications | Scheduled reminders; push to phones; quiet hours | Notification service; user profiles | Low–Med | Snooze everywhere; quiet-hours enforced | Missed chores/events drop noticeably |
| v0.3.0 | Kitchen Hub MVP | Tablet “Today” dashboard; calendar view (read-only); chore queue; alerts | Tablet mount/placement; web UI | Low–Med | Big simple UI; offline-ish fallback | Tablet replaces mental load for “what’s today?” |
| v0.4.0 | One-tap Logging + Routines | Buttons: “Fed rabbits”, “Topped water”; routine cards (Film Night / Bedtime) | Routine definitions; state tracking | Med | Confirmations; undo for 2 minutes | You can run routine + log chores in <10 seconds |
| v0.5.0 | Reliability & Observability | Backups; restore; basic uptime monitor; error alerts | Scheduled jobs; logs | Med | Rollback plan; “safe mode” | A break doesn’t nuke your data |
| v0.6.0 | Data Model Hardening | Defined entities: People, Chores, Animals, Inventory items; export/import | Schema + migration plan | Med | Migration scripts; versioned schemas | Future features don’t require rework |
| v0.7.0 | Voice Read-Only | “Hey Elias” wake; STT; TTS responses; status queries | Mic device; STT/TTS; wake word | Med | Read-only only; rate limit; quiet-hours | Voice answers reliably without accidental triggers |
| v0.8.0 | Permissions & Audit | Action catalog framework (even if unused); audit log; roles | Auth method; RBAC | Med | Allowlist only; logs retained; admin approval | Actions are impossible without explicit permission |
| v1.0.0 | Stable Daily Use | Hardened UX; runbooks; update process; “family proof” | Documentation; testing checklist | Med | Change control; release notes; rollback | You trust it daily without babysitting |
| v2.0.0 | Voice Actions (Controlled) | Timers; reminders; lights/plug toggles; confirmations | Smart home integration; action catalog | High | 2-step confirm for sensitive actions; scoped permissions | Voice can do limited actions safely |
| v2.5.0 | Advanced Household Ops | Calendar writes; chore assignments; “nagging but kind” coaching | Calendar API integration; profiles | High | Approval flows; “no spam” throttle | It helps without becoming annoying |
| v3.0.0 | Meal Planning + Inventory | Inventory-lite; use-it-first list; meal suggestions; grocery list | Inventory input method; rules | High | Conservative food safety; “uncertain → don’t advise” | Less waste + easier meal decisions |
| v3.5.0 | Livestock-aware Waste Routing | “rabbit/chicken/compost” guidance for leftovers | Livestock ruleset; safety checks | High | Strict safe-list; disclaimers; require confirmation | It avoids dangerous feeding advice |
