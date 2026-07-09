# Feasibility Checker — example

The Allergy Parents brief (see the [Brief Builder example](../brief-builder/example.md))
goes in for its gut-check. All names fictional. A short B2B contrast example
follows.

## What the user pasted in

The full brief from the Brief Builder: US parents of children under 18 with
an HCP-diagnosed food allergy, n=400, assumed IR 20% (client guess), LOI 15
min estimated, quotas by child age band (0–5 / 6–12 / 13–17, ~133 each, not
interlocked), mobile-friendly, launch June 11, hard close June 21.

## What the Feasibility Checker returned

```
FEASIBILITY RISK ASSESSMENT — Meridian Foods / Allergy Parents

OVERALL RISK: MEDIUM-HIGH
The audience itself is reachable — food-allergy parents exist in every
consumer panel. The risk concentrates in one place: the 20% IR is a
client guess that rough prevalence logic suggests is optimistic, and it
sits under a hard 10-day deadline with no recovery room. If the IR
assumption fails, everything downstream fails with it.

RISK TABLE
| Dimension | Risk | Why |
|---|---|---|
| Audience rarity | Medium | Niche-ish consumer audience; parents of a diagnosed-condition child, not gen pop — but not B2B-rare |
| Market depth | Low | US consumer panels are the deepest available |
| n vs. audience | Medium | 400 is achievable for this audience in the US, but not trivially in 10 days if IR runs low |
| Quota structure | Medium | Three ~133 cells, not interlocked — sane. Watch 13–17: allergies are diagnosed young, so panels may skew toward parents of younger children |
| LOI | Low | 15 min estimated is workable, but it's untested — if it fields at 20+, dropout rises |
| Timeline | High | 10 field days, HARD deadline (client QBR), no slack for a re-quote or IR surprise |
| IR assumption quality | High | "Maybe 1 in 5" is a guess with no stated **base** — 20% of what? Published estimates put diagnosed food allergy at roughly ~8% of US children (approximate — definitions vary); parent-level incidence runs somewhat above per-child prevalence (a parent of several children has better odds that ≥1 is affected), but 20% of *general-population* entrants is not close, and even against a parents-only base it looks optimistic. The unstated base is itself a finding. |

THE RISKIEST COMBINATION
Optimistic IR × hard deadline. Illustration only — the arithmetic your
own assumptions imply: at 20% IR measured against parent-targeted
entrants and ~75% completion, ~2,700 entrants deliver n=400. If real IR
on that same base is ~8–10%, that entrant load roughly doubles,
and you'd discover it on day 2–3 of a 10-day window with no room to
re-plan. ASSUMPTION: ~75% completion is a placeholder — your soft launch
will give you the real number.

WHAT WOULD CHANGE THIS ASSESSMENT
- Any past fielding data on this audience (yours or a supplier's) — this
  is the single most valuable missing fact
- Whether the client would accept "parent-reported HCP diagnosis" vs.
  stricter verification (wording moves IR materially)
- Whether n or the age-band quotas have any flex

MITIGATIONS (in order of impact)
1. Re-anchor the IR in the RFP: state 20% as the client's assumption and
   explicitly ask each supplier for THEIR estimate and its basis. Their
   answers are a free feasibility study.
2. Mandate a day-1 soft launch (~10%) with a same-day IR/LOI readout,
   and pre-agree with the client what happens if IR comes back under 10%
   (drop a quota cell? extend? reduce n?). Decide this BEFORE launch —
   there's no time to negotiate it on day 3.
3. Ask suppliers to quote the 13–17 cell feasibility separately — it's
   the likeliest stall.
4. If the client can move the QBR read-out to topline-only, fielding
   gains ~3 days of real slack.

QUESTIONS TO PUT TO SUPPLIERS
1. What IR are you assuming for this spec, on what base (general-
   population entrants, or parent-pre-targeted?), and what is it based
   on? The same rate on different bases is a different project.
2. What does your feasibility look like for the 13–17 age-band cell
   specifically, in the 10-day window?
3. If actual IR runs materially below your assumption, what happens to
   price and timeline — exactly?
4. What soft-launch readout can you give us within 24 hours of launch?
```

## B2B contrast (mini example)

Same agent, different spec: **US IT decision-makers at 500+ employee
companies, n=150, LOI 20 min, 10 field days.** The shape of the answer
changes completely: audience rarity and market depth become the High-risk
rows ("senior B2B titles are among the scarcest, most fraud-targeted sample
that exists"), the riskiest combination becomes *n=150 × seniority × 20-min
LOI* rather than IR × deadline, and the top mitigation becomes asking
suppliers about verification methods and blend transparency, not soft-launch
timing. Same format, same honesty — different judgment.

## Why this example matters

The agent never said "this project is infeasible" — and never said "you'll
be fine." It located the risk (IR quality × hard deadline), showed the
arithmetic *as arithmetic*, cited prevalence as approximate context rather
than fact, and converted every concern into either a mitigation or a
supplier question. That's the entire job.
