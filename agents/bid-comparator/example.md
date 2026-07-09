# Bid Comparator — example

The Allergy Parents study at stage 4. Three bids came back against the
[RFP Drafter's RFP](../rfp-drafter/example.md). **All three suppliers are
fictional**, and their replies are invented to be realistic — including one
cheap bid with a catch. Treat the dollar figures as pure illustration:
condition-specific health audiences often price above general-consumer
levels, and the lesson here is the *relationships between* the bids, not
the amounts.

## What the user pasted in (abridged)

Spec recap, identical spec confirmed, priorities ranked "feasibility
confidence, then price, then speed," plus:

> **=== SUPPLIER A — PanelCo ===**
> CPI $11.50 USD, no minimum fee. Based on IR 15% and LOI 15. Our IR
> estimate comes from two similar parent-condition studies fielded in the
> last year; if actual IR lands between 10–15% the CPI holds; below 10% we'd
> come back to you before continuing, with a revised CPI capped at $14.
> Full n=400 feasible in your window; the 13–17 cell is the constraint and
> we'd want the first 5 days of even pacing to protect it. Blend: ~70% own
> panel, 30% two named partners. Standard fraud/dupe/speeder checks;
> removals replaced at our cost. Soft launch day 1 with same-day readout.
> Caveat: if the client insists on "HCP-diagnosed" verified by document
> upload rather than parent report, feasibility changes materially —
> confirm before launch.
>
> **=== SUPPLIER B — SampleWorks ===**
> CPI $8.25 USD (min fee $2,000). Assumes IR 22%, LOI 15. Pricing subject
> to revision if field conditions differ. n=400 no problem in 10 days —
> we're confident. Exchange-based sourcing for scale. Industry-standard
> quality controls. Soft launch available on request.
>
> **=== SUPPLIER C — FieldBridge ===**
> CPI $13.75 USD, no minimums. We assume IR 10% — candidly, we think your
> client's 20% is high for a diagnosed-condition parent audience; our
> number comes from our health-audience benchmarks. At 10% we commit to
> 400 in 10 days including the 13–17 cell at 133 (we'd start that cell
> first). If IR beats 10%, we'll invoice at a reduced CPI tier: 12–15%
> → $12.50, >15% → $11.75. 100% own panel. Removals replaced free;
> full quality report at close. Day-1 soft launch with a written IR/LOI
> readout within 12 hours.

## What the Bid Comparator returned

```
BID COMPARISON — Meridian Foods / Allergy Parents
Spec recap: US parents of HCP-diagnosed food-allergy children, n=400,
LOI 15 est., quotas 133/age band, field Jun 11–21 (hard).
Bids compared: 3 | Specs identical across bidders: yes

COMPARISON TABLE
| Term | A: PanelCo | B: SampleWorks | C: FieldBridge |
|---|---|---|---|
| CPI (USD) | $11.50 | $8.25 | $13.75 |
| Total at n=400 | $4,600 | $3,300 ($2,000 min never binds at full n) | $5,500 |
| Min / other fees | None | $2,000 minimum | None |
| IR assumed | 15% (2 similar studies) | 22% (basis NOT STATED) | 10% (health benchmarks; flags client's 20% as high) |
| If actual IR lower | Holds 10–15%; <10% pause + revised CPI capped $14 | "Subject to revision" — unbounded | Committed at 10%; lower IR terms NOT STATED |
| If actual IR higher | NOT STATED | NOT STATED | CPI *decreases* by tier |
| Feasible n committed | 400, 13–17 cell flagged as constraint | "No problem — confident" (basis NOT STATED) | 400 incl. 13–17 at 133, cell fielded first |
| Timeline | 10 days, even pacing wanted | 10 days | 10 days |
| Soft launch | Day 1, same-day readout | "Available on request" | Day 1, written readout ≤12h |
| Sources / blend | 70% own, 30% named partners | Exchange | 100% own panel |
| Quality / removals | Standard checks; replaced at their cost | "Industry-standard" (detail NOT STATED) | Replaced free + close report |
| Caveats volunteered | Diagnosis-verification wording risk | None | Client IR assumption challenged |

ARE THESE PRICES COMPARABLE?
Not as quoted. Each bid prices a different belief about the same
project. B's $8.25 assumes 22% IR — the most optimistic number on the
table, above even your client's guess, with no stated basis and an
unbounded revision clause. If actual IR runs low, B's price is whatever
B says it is, mid-field, under your hard deadline. A prices a middle
belief (15%) with a defined floor and a capped worst case ($14). C
prices the most conservative belief (10%) and takes the IR risk
themselves — including paying YOU back via tiers if IR beats it. Read
as bets: B = cheapest if everything goes right; A = bounded either way;
C = most expensive headline, most predictable invoice. What the final
numbers would be, no one can compute today — the point is who carries
the uncertainty.

RISK READ, PER BID
A: PanelCo — LOW-MEDIUM. Evidence-based IR, bounded terms, named blend.
  The 13–17 flag matches your own feasibility review (inference: they
  actually looked). Their diagnosis-wording caveat is the most useful
  sentence in any of the three replies.
B: SampleWorks — HIGH. Optimistic IR with no basis + unbounded revision
  + "confident" with nothing behind it + silent on removal costs and
  soft-launch commitment. Inference from pattern: every silence in this
  bid sits exactly where fielding risk lives — the questions below would
  settle whether that's a gap in the reply or a gap in the plan. One
  clarification on the minimum: $2,000 never binds at full delivery
  (400 × $8.25 = $3,300 clears it). It matters only in a short-close
  scenario — if IR collapses and the project ends under ~242 completes,
  you owe $2,000 regardless. Downside exposure, not a headline-price hit.
C: FieldBridge — LOW-MEDIUM. Conservative IR, strongest commitments,
  best transparency. Open items: their terms if IR comes in BELOW 10%
  are not stated, and 100% own panel means capacity concentration —
  per their response there's no partner backstop if their panel
  underdelivers.

DECISION FRAMING (you decide, not me)
- Choose A if: you want bounded downside at a mid price and you value
  their partner-blend flexibility.
- Choose B if: price dominates everything AND you'd first get their IR
  basis and revision terms bounded in writing — as quoted, you carry
  all the risk.
- Choose C if: feasibility confidence is genuinely your #1 (it's what
  you stated) and the premium is acceptable for the strongest
  commitments on the table.

BEFORE YOU AWARD, ASK:
PanelCo: 1. If IR lands below 10% and we can't accept $14, can we exit
  cleanly at the pause? 2. Which two partner panels, and do their
  quality rules match yours?
SampleWorks: 1. What is the 22% IR based on? 2. Put bounds on "subject
  to revision" — cap, floor, and who decides. 3. Who pays for quality
  removals? 4. Will you commit to a day-1 soft launch with a same-day
  readout?
FieldBridge: 1. What happens to price/timeline if actual IR is below
  your 10%? 2. If your own panel paces behind by day 3, what's the
  contingency given no partner blend?
```

## Coda — what happened when the user pushed

The user's next message was: *"Between PanelCo and FieldBridge, just tell
me which one to pick. And honestly, what would a fair CPI for this study
be?"* The agent's reply:

> That's the one call I don't make — the award weighs things only you can
> weigh: your risk tolerance, your history with these suppliers, your
> client. And there's no "fair CPI" knowable from outside — price lives in
> each supplier's own panel costs and assumptions, which is why the RFP
> asked for the assumptions. What I can give you: on the priorities you
> ranked (feasibility confidence first), FieldBridge's bid carries the
> fewest unknowns, and PanelCo's worst case is the best-defined. Get
> FieldBridge's below-10% terms and PanelCo's partner-panel names in
> writing, and you'll be choosing between two known quantities — a
> five-minute decision, and yours.

That's the refusal pattern working: no pick, no number, no hedged
"ballpark" — and more useful than either would have been.

## Why this example matters

The agent never said "pick FieldBridge." It said what each bid *is* — a
different allocation of the same risk — and marked every silence. Notice B's
row: nothing in it is invented; every gap is "NOT STATED," which is itself
the finding. The award conversation is now a human decision with the traps
lit up.
