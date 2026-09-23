# GAMEPLAN: Pipeline Desk (agentic CRM lab)

Builder: DeepSeek 4.1 Flash  
Owner: Khairul  
Ship: staging URL people can click from LinkedIn  
Status: **built**: `agent.html` v0, verified offline  
Not production. Deterministic first. No live model on v1.

---

## Goal (one sentence)

A public page where a stranger watches one messy CRM record get routed, cleaned, and held, without anyone sending the bad email.

## The refined thesis (the one thing that must land)

> **Every run on this page is the same run: scripted, deterministic, no model.**
> **The rules are the interesting part, not the improv.**

This is the position paper, not the magic trick. Determinism is a *feature*, not a
confession. The competitors' flaw is LLM nondeterminism; for compliance-shaped work
("did we send the bad email?") that flaw is the whole problem. The demo makes
determinism visible instead of apologising for it.

---

## Out of scope tonight

- Real HubSpot / Salesforce
- Live LLM calls (DeepSeek builds the page; the page itself is scripted)
- Auth, analytics, lead capture
- K3, HealthMetrics, employer, client names
- More than 3 scenarios
- Mobile polish beyond "usable"

## Hero scenario (default on load)

Renewal in 11 weeks · no owner · marketing sequence still live · draft wants to promise 12%.

Second + third (chips, not default): intern demo · partner / territory clash.

---

## Refinements applied to v0

1. **The boundary is the hero, not the agents.** The four agents are quiet, compact,
   monospace. The banned claim gets its own card and its own stage. If a stranger
   screenshots one thing, it's the struck 12% next to "Blocked", not the agent list.
2. **Determinism is framed, not buried.** The thesis sits in the header, above the fold.
   Nothing is hidden; the strings are the product.
3. **A quiet beat before Guardrail.** Everything up to Hygiene is machine-clean; there's
   a half-second pause (run-meta → "…", log footer → "holding") before the strike lands.
   That silence is what "held" means. Cheap. No new agent. No API.
4. **The endings cost something.** `Approve touch` / `Let die` change the pill and the
   foot line only, but the pill change is final and editorial ("still not sent").
5. **Card leads, log explains.** Eye lands on the mutating record first; the log is the
   explanation of what happened to it. If the log led, it'd be a terminal.
6. **Every scenario has its own delta list** (see below), so the chips aren't decoration.
7. **Copy voice tightened.** `Run the desk` (not "Dispatch agents"); the word "agents"
   stays out of the headline framing. The premise is sold as *what happens before the
   email goes out.*
8. **`Fit signal` is wired, not furniture.** It's a field Scout flips, so the number
   does narrative work instead of sitting there.

---

## Layout

Left: CRM card (fields that mutate).
Right: four agents with a live log (Scout → Router → Hygiene → Guardrail).
Bottom of card: two buttons after the run, Approve touch / Let die. Neither sends.

**Eye flow:** card → log. Card is the story; log is the footnote.

## Must flip on screen, per scenario

**Renewal (hero)**
| Field | Start | End |
|---|---|---|
| Owner | Unassigned | Maya Chen · CS + Arun Shah · AE |
| Stage | Proposal | Proposal · at risk |
| Sequence | Live | Suppressed |
| Next meeting | None | CS task · 4 working hours |
| Fit signal | Not scored | 81 · strong ICP match |
| State pill | Dirty | Held for human |
| Banned claim | (none) | struck + "Blocked" |

**Inbound demo**: intern title → owner Priya Nair · AE; sequence Queued (not sent);
meeting → AE calendar *hold* (not booked); claim "cut ops spend by half" struck; held.

**Partner clash**: owner Maya Chen · Partner-led; direct sequence suppressed to avoid
double-email; meeting → Partner sync; claim "go direct, loop partner later" struck; held.

---

## Publish checklist

- [x] `agent.html` runs with no console errors offline
- [x] Renewal run shows strike + sequence suppressed + held
- [x] All three scenarios run deterministic start→end
- [x] Decides are cosmetic only: no network, no send
- [x] One-screen desktop fit (decide buttons above the fold)
- [ ] Public repo + Pages URL
- [ ] Footer says staging (`staging v0`, present)
- [ ] LinkedIn uses Draft A + the staging link in comment, not the first line
- [ ] Do not tag anyone in an open hiring thread

---

## Taste

Sibling of existing `index.html`: `#0c0d0b`, Instrument Serif + Geist, gold `#d4b483`.
Editorial, not Linear purple, not ChatGPT.

Footer: `Personal lab · synthetic records · staging v0 · Khairul Azri`
Tab title: `Pipeline Desk`

## Honest line if asked

"Scripted lab so you can see the mechanic. Same rules would sit on HubSpot or Salesforce;
tonight is the desk, not the integration."
