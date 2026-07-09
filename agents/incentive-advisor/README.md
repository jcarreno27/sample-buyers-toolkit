# Incentive Advisor

Recommends respondent incentive ranges using opportunity-cost logic: what
the respondent's time is worth × how you're reaching them × how scarce they
are — with tiers, floors, and the two rules people skip (price to the
hardest quota cell; incentive ≠ CPI). Built from the author's B2B fieldwork;
it states plainly when an audience is outside its calibration.

This is the kit's one cross-cutting specialist rather than a lifecycle
stage: consult it after the brief and feasibility check, before the RFP —
and again whenever a bid's CPI looks too close to what the respondent
would need to receive.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a
   new chat in Claude, ChatGPT, or Gemini (or into a Claude Project /
   Custom GPT / Gem as instructions).
2. Describe audience, sourcing method, and LOI — the
   [input template](input-template.md) covers the rest.
3. You get an anchored range with three tiers, every adjustment named so
   you can challenge it, and the supplier questions that keep the
   incentive honest.

**Claude Code users:** copy the skill folder instead —
`cp -r claude-code-skill ~/.claude/skills/incentive-advisor`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | Fill-in request form |
| [output-template.md](output-template.md) | What the recommendation looks like |
| [example.md](example.md) | B2B run + the agent declining to fake consumer calibration |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

Feeds the [RFP Drafter](../rfp-drafter/) (state the intended incentive and
bids come back comparable), arms the [Bid Comparator](../bid-comparator/)
("that CPI is near the incentive itself — what does the respondent
receive?"), and disciplines the [Fielding Risk Advisor](../fielding-risk-advisor/)
conversation when "just raise the incentive" gets proposed mid-field.
