# Changelog

All notable changes to this kit are documented here.

## 1.1.1 — 2026-07-08

Refinements from continued review:

- **Fixed a unit error in the incentive anchor** — the written formula
  multiplied dollars/hour by LOI *minutes*; now explicitly
  `comp ÷ 2,080 × (LOI minutes ÷ 60)` everywhere it appears
- **Canon guardrail 1 reworded** from "never give" to "never originate" a
  price — repeating user-pasted figures with attribution is explicitly part
  of the job (this removed a literal-reading conflict with the Bid
  Comparator's core task)
- Incentive Advisor: qualifier loading re-rationalized (pays for burden,
  verification, and reluctance — rarity's cost lands in CPI, not
  incentive); example arithmetic now shown transparently and range
  corrected to follow it; **regime now gates the output** (no consumer
  range without user norms; no HCP numbers without FMV guidance)
- Screener strictness bands re-labeled as rough B2B priors for spotting
  order-of-magnitude mismatches — never a way to derive an IR from a label
- Delivery-shape heuristic conditioned on full release into open quotas —
  staged releases, throttling, and resend waves legitimately flatten the
  curve; ask about cadence before inferring hidden sourcing
- ChatGPT install paths corrected: full kit exceeds Custom GPT instruction
  limits (first-message route documented); Custom GPT creation noted as
  paid-plan; "no accounts" claim softened to "nothing new to sign up for"
- Root README full-kit references corrected from six to seven agents

## 1.1.0 — 2026-07-08

**New agent: Incentive Advisor** — recommends respondent incentive ranges
via opportunity-cost logic (time value × access premium × scarcity), with
tiers, floors, the hardest-quota-cell rule, and explicit calibration
honesty (B2B-calibrated; consumer/HCP direction-only). Graduated from the
roadmap.

**New doc: `docs/practitioner-benchmarks.md`** — field-tested starting
values from the author's fourteen years on the supplier side: the
five-layer feasibility funnel, panel-overlap rule (1+1 ≠ 2), panel timeline
saturation ("add sources, not weeks"), the completes-by-week delivery-shape
check, LOI decay, screener-strictness pass-rate bands, incentive logic, and
supplier-quote diagnostics. Paste-ready for any agent's benchmarks block.

**Hardened guardrail canon (now six items, all agents + full kit):**
- Closed the "exact CPI" loophole — no ranges, no anchors, no "ballpark,"
  no implying a fair price
- Added the refusal-plus-alternative pattern for "just give me a number"
  pressure (demonstrated in the Bid Comparator example's new coda)
- Inference labeling required alongside assumption labeling
- Bid Comparator and Fielding Risk Advisor prompts now carry their
  agent-specific stricter items (no winner/motive reads; no blame)

**Domain sharpening from external review:**
- IR now always asks for its **base** (gen-pop vs. pre-targeted frame) —
  brief checklist, RFP requirements, feasibility example, glossary
- Fixed minimum-fee analysis in the Bid Comparator example (a floor, not
  an additive charge)
- Feasibility/fielding/questionnaire examples corrected (band-merge
  mitigation, no invented supplier terms, LOI component math reconciled,
  child-health consent flag)
- Glossary: added concealed-list screener, quota gate, attention/
  consistency check, fatigue cliff; RFP and fielding templates synced to
  their agent versions

## 1.0.0 — 2026-07-08

Initial release.

- Six agents: Brief Builder, Feasibility Checker, RFP Drafter, Bid Comparator,
  Questionnaire Risk Reviewer, Fielding Risk Advisor
- Full-kit prompt with stage router, plus per-agent standalone prompts
- Fill-in templates for intake, RFPs, supplier responses, fielding updates,
  and questionnaire reviews
- Claude Code skill versions of all six agents
- Documentation: how to use, agent selection guide, full workflow example,
  benchmark customization, procurement basics, limitations, privacy, glossary
