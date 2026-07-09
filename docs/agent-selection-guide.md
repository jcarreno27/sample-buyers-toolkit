# Which agent do I need?

Start from what's in front of you right now.

| What's in front of you | Agent |
|---|---|
| A pile of emails/notes that needs to become a spec | [Brief Builder](../agents/brief-builder/) |
| A brief, and the question "can this actually be fielded?" | [Feasibility Checker](../agents/feasibility-checker/) |
| A brief that needs to become supplier emails | [RFP Drafter](../agents/rfp-drafter/) |
| Supplier quotes that need comparing | [Bid Comparator](../agents/bid-comparator/) |
| A screener/survey about to launch | [Questionnaire Risk Reviewer](../agents/questionnaire-risk-reviewer/) |
| In-field numbers, a soft-launch readout, or a mid-field supplier request | [Fielding Risk Advisor](../agents/fielding-risk-advisor/) |
| "What should we pay respondents?" — or an incentive that needs a sanity check | [Incentive Advisor](../agents/incentive-advisor/) |

## By the question you're asking

- "What do I even tell suppliers?" → **Brief Builder**
- "Is my client's IR assumption sane?" → **Feasibility Checker**
- "Why does every bid assume something different?" → your RFP; next time use
  the **RFP Drafter**, this time use the **Bid Comparator**
- "Why is the cheap bid cheap?" → **Bid Comparator**
- "How is that CPI even possible — what's the respondent getting?" →
  **Incentive Advisor** (anchor) + **Bid Comparator** (the question)
- "What incentive should the RFP state?" → **Incentive Advisor**, after the
  feasibility check, before the RFP goes out
- "Will this survey field OK on phones?" → **Questionnaire Risk Reviewer**
- "Topline looks fine but something feels off" → **Fielding Risk Advisor**
- "IR is reading way below what we bought" → **Fielding Risk Advisor** first
  (what to do now), then **Questionnaire Risk Reviewer** if a screener leak
  is suspected

## Common situations

**"I do all of this, constantly."** Install the [full kit](../full-kit/) as
a Claude Project or Gemini Gem and keep it open all day. (In ChatGPT, paste
it as the first message of a long-running chat — the full kit outgrows
Custom GPT instruction limits.)

**"I'm mid-crisis, in field, right now."** Fielding Risk Advisor. Paste the
numbers you have, say "just proceed," and you'll get the decide-now list.

**"I've never bought sample before."** Read
[sample-procurement-basics.md](sample-procurement-basics.md) (5 minutes),
then start with the Brief Builder — it teaches the spec by asking for it.

**"My problem is the client, not the suppliers."** The Feasibility Checker's
written risk assessment is built to be forwarded: it says *why* the ask is
risky in neutral language, which beats "trust me, that's hard."

## What nothing in this kit does

Design research, pick your suppliers, negotiate for you, predict prices, or
replace your judgment. See
[limitations-and-guardrails.md](limitations-and-guardrails.md).
