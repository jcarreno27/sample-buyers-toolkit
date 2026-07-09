# Fielding Risk Advisor — example

The Allergy Parents study at stage 6: day 4 of 10 in field with FieldBridge
(fictional supplier). The screener was fixed per the
[Questionnaire Risk Reviewer's example](../questionnaire-risk-reviewer/example.md).
The topline looks fine. It isn't.

## What the user pasted in

```
FIELDING UPDATE — Meridian Foods / Allergy Parents — Day 4 of 10

TARGETS & BOUGHT ASSUMPTIONS
Total completes needed: 400
Window: Jun 11–21, HARD
IR awarded on: 10% | LOI awarded on: 15 min

ACTUALS SO FAR
Completes: 178 of 400
Actual IR: 11% (soft launch read 12%)
Median LOI: 17 min
Drop-off: 14%
Quality removals: 9 (replaced)

QUOTA STATUS
0–5: 71 of 133 | 6–12: 83 of 133 | 13–17: 24 of 133

SUPPLIER SIGNALS
Last update: yesterday — "pacing well overall, watching the teen cell"
No change requests. Soft launch ran day 1, readout within 12h as
committed.

YOUR READ
Topline seems fine? Teen cell feels slow but we have 6 days.
```

## What the Fielding Risk Advisor returned

```
FIELDING RISK READ — Allergy Parents — Day 4 of 10

TRAJECTORY RISK: MEDIUM-HIGH
The project's real deadline isn't June 21 — it's whenever the 13–17
cell becomes unfillable, and that cell is the whole story of this
update. Topline pace and IR are genuinely healthy; the risk is
concentrated, which is good news only if you act on it this week.

ACTUALS VS. BOUGHT ASSUMPTIONS
| Metric | Bought | Actual | Divergence read |
|---|---|---|---|
| IR | 10% | 11% | Better than bought — the concealed-list screener is doing its job |
| Median LOI | 15 | 17 | Mild inflation; FieldBridge quoted no LOI-adjustment term, so this isn't a contractual cost event — confirm that reading with them before it inflates further |
| Pace | 40/day avg needed | 44.5/day | Ahead on topline — but see quota balance |
| Quota balance | ~33% each cell by now | 0–5: 53%, 6–12: 62%, 13–17: 18% | One cell is starving while two overfill |
| Quality removals | replaced free | 9, replaced | Unremarkable |

TRAJECTORY FLAGS
- The arithmetic (as arithmetic): 13–17 needs 109 more completes in 6
  days ≈ 18/day. Demonstrated rate for that cell: 6/day. The two easy
  cells will hit their caps within ~2–3 days at current rates (and
  those rates will slow), at which point ALL remaining sample must come
  from the hardest cell — the exact "make it up at the end" shape that
  fails.
- Fielding is front-loaded: day-7-to-10 daily rates are typically the
  project's slowest. An 18/day requirement against a 6/day
  demonstrated rate is not a gap that time fixes on its own.
- FieldBridge said at bid they'd field 13–17 FIRST (per their
  response). 18% fill at day 4 doesn't look like "first." Worth asking
  directly — pattern noted, no conclusion drawn.

DECIDE NOW (gets more expensive daily)
1. Pre-agree the fallback with your client TODAY, while options exist:
   accept 13–17 under target (readability tradeoff named), extend for
   that cell only, or widen the read (e.g., merge 6–12 and 13–17 into
   a single 6–17 cut — trading age granularity for fill). On day 8 the
   only option left is "under target."
2. Decide whether to cap the 0–5 and 6–12 cells now — every over-fill
   there is spend and panel goodwill not aimed at the constraint.

ASK YOUR SUPPLIER (specific, numbers in)
1. "13–17 is at 24 of 133 with a demonstrated 6/day. You committed to
   fielding this cell first — what specifically is running, and what
   daily rate will you commit to for the next 3 days?"
2. "If your answer is under 15/day: what would unlock more — targeted
   re-contacts, partner sources (you bid 100% own panel — what's the
   contingency?), or an incentive bump, and at whose cost?"
3. "Median LOI is reading 17 vs. 15 tested. Where in the survey is the
   drop-off concentrated?"

WATCH FOR NEXT UPDATE
- 13–17 daily rate: under 10/day tomorrow promotes decision #1 from
  "pre-agree fallback" to "trigger fallback."
- Drop-off: above ~18% suggests the LOI inflation is starting to bite.
- ASSUMPTION: quota fills you pasted are as-of-today; if they're
  yesterday's, ask for a same-day cut before acting.
```

## Why this example matters

The user's read was "topline seems fine" — and the agent agreed the topline
was fine *and showed why that was the wrong question*. Note what it didn't
do: no "you'll close at 360" prediction, no "FieldBridge is dropping the
ball" accusation (it flagged the commitment-vs-pattern gap and drafted the
question instead), and both mitigations came with their costs named. The
supplier questions have numbers in them — those get answered; "any update on
the teen cell?" gets "watching it."
