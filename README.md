# Pipeline Desk

A personal RevOps lab. Watch one messy CRM record get routed, cleaned, and **held** —
without anyone sending the bad email.

**Not a CRM product. Synthetic records. Deterministic by design.**

---

## What this is

A single self-contained HTML page (`agent.html`) that plays a scripted 8-second run:

- **Scout** — enrich, find the open opp, check for duplicates
- **Router** — assign an owner and an SLA
- **Hygiene** — suppress the live sequence, flag the stale stage
- **Guardrail** — draft a note, **strike the banned claim, do not send**

Same input → same run, every time. No model. No API. No network.

## Why deterministic

The interesting part of agentic work isn't the improv — it's the rules. For
compliance-shaped decisions ("did we send the bad email?"), reproducibility *is* the
feature. This page makes that visible instead of apologising for it.

## Scenarios

- **Renewal** (default) — renewal in 11 weeks, no owner, sequence still live, draft wants
  to promise 12%.
- **Inbound demo** — intern title, AE calendar held not booked.
- **Partner clash** — no double-email; direct sequence suppressed.

## Files

```
agent.html     ← the demo (open this)
index.html     ← landing page, links to the demo
GAMEPLAN.md    ← the spec and rationale
```

No bundler. No npm. Open `agent.html` in a browser.

## Honest line

Scripted lab so you can see the mechanic. Same rules would sit on HubSpot or Salesforce;
this is the desk, not the integration.

---

Personal lab · synthetic records · staging v0 · Khairul Azri
