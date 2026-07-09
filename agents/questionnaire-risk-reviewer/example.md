# Questionnaire Risk Reviewer — example

The Allergy Parents study at stage 5: FieldBridge won the award, launch is
in four days, and the draft questionnaire arrives for a fielding read. All
names fictional; the questionnaire flaws are deliberately classic.

## What the user pasted in (abridged)

Context (audience, n=400, quotas by child age band, assumed IR now 10% per
the awarded bid, claimed LOI 15 min *estimated*, majority-mobile expected),
plus the screener and survey. Key excerpts:

> S1. Do you have a child under 18 who has been diagnosed with a food
> allergy by a doctor? (Yes / No — No TERMINATES)
> S2. What is your child's age? (open numeric)
> S3. Which food is your child allergic to? (single select: peanuts, tree
> nuts, milk, eggs, other)
> ...
> Q8–Q11. Four brand-perception grids, each 9 rows × 7-point scale
> Q12. "Please describe in detail a recent experience shopping for
> allergy-safe foods." (required, minimum 200 characters)
> ...
> [Survey totals 58 questions. No attention checks. Routing notes exist
> for the screener only.]

## What the Questionnaire Risk Reviewer returned

```
QUESTIONNAIRE FIELDING-RISK REVIEW — Meridian Foods / Allergy Parents

RISK SUMMARY
| Dimension | Risk | Why |
|---|---|---|
| IR / screener | HIGH | S1 telegraphs the qual in question one — anyone who wants in knows to say yes |
| LOI | HIGH | 58 questions incl. 4 large grids + a 200-char required open-end doesn't fit 15 min (arithmetic below) |
| Quotas | MEDIUM | S2 captures one child's age, but quotas are per allergic child — multi-child households route ambiguously |
| Mobile | MEDIUM-HIGH | Four 9×7 grids back-to-back; 200-char required typing on phones |
| Fraud & quality | HIGH | Guessable screener + zero attention/consistency checks + child-health topic (fraud-attractive) |
| Drop-off | MEDIUM | Q12's required long open-end sits right after the grid fatigue cliff |

LOI REALITY CHECK (illustration, not prediction)
58 questions total: ~53 closed single-selects ≈ 8–10 min, four 9-row
grids ≈ 4–6 min, the required 200-char open-end on mobile ≈ 2–3 min,
plus the screener ≈ 1 min.
Rough total: 15–20 min BEFORE any respondent slows down — and this
assumes clean pace. The 15-min claim is the optimistic edge of the
range. ASSUMPTION: standard per-item timings; your soft launch
measures the truth. If it fields at 18+, your CPI assumptions and
drop-off both move against you.

QUESTION-BY-QUESTION FLAGS
S1 — Telegraphs the qualification — inflated fake "yes" rate, fraud
  magnet, and your apparent IR becomes unreadable — Restructure as a
  concealed list: "Which of the following has a doctor diagnosed any of
  your children with?" with food allergy among 6–8 conditions incl.
  plausible decoys; qualify from the list.
S2 — Captures one child's age, but the quota is the ALLERGIC child's
  age band, and multi-child households are common — Ask the age of the
  child WITH the diagnosed allergy (and handle multiple allergic
  children explicitly: e.g., youngest such child).
S3 — Fine as a question, but as a single-select it can't handle
  multi-allergy children (very common) — Make multi-select; also a free
  consistency check later (S3 vs. a Q30 re-ask catches fraud cheaply).
Q8–Q11 — Grid streak = fatigue cliff and mobile misery — Break up the
  sequence; consider trimming rows (do all 9 brands matter per grid?).
Q12 — Required 200-char minimum on mobile right after the grids —
  Make it optional or drop the minimum; you'll get better text from
  fewer, willing respondents than forced filler from everyone.
(no routing notes exist for the main survey — FINDING: get them in
  writing before launch; skip-logic errors found in field cost days)

THE ONE CHANGE THAT MATTERS MOST
Fix S1. Every other risk here degrades the project; a telegraphed
screener invalidates it. With a concealed-list screener, your measured
IR means something, fraud gets harder, and FieldBridge's 10% assumption
gets a fair test. It's a 20-minute edit.

WHAT TO TELL YOUR SUPPLIER BEFORE LAUNCH
- This survey collects health information about a minor, reported by a
  parent. Confirm consent language and health-data handling meet your
  and your client's compliance requirements before launch — flagged
  here, but this review can't certify compliance.
- The screener is being restructured to a concealed list — re-confirm
  their IR estimate against the new wording.
- LOI arithmetic suggests 15 min is optimistic; ask them to flag the
  soft-launch median immediately, and agree now what happens if it
  reads 18+.
- No attention checks existed; two are being added — confirm their
  removal/replacement policy covers failures on these.
```

## Why this example matters

The review stayed in its lane — nothing about whether brand-perception
grids answer Meridian's research questions — and every flag connects a
questionnaire feature to a *fielding consequence*. Note the LOI check is
shown as arithmetic with an explicit "soft launch measures the truth"
caveat, and the S1 fix is a direction, not a rewritten screener.
