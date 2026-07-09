# Fielding Risk Advisor

Reads your in-field updates the way a veteran PM does: compares actuals to
the assumptions the project was bought on, finds the quota cell quietly
starving behind a healthy topline, and sorts everything into **decide now /
ask your supplier / watch**. Catches field trouble while it's still cheap.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions). For pulse checks, keep one ongoing chat so it
   sees the trend.
2. Paste your fielding update — the [input template](input-template.md)
   shows what to include. Numbers beat adjectives.
3. You get a trajectory-risk read, an actuals-vs-assumptions table, and the
   three-bucket action sort with supplier questions that have numbers in
   them.

**Optional — only if you use Claude Code** and would prefer to install
this agent as an auto-activating skill. Once you've downloaded the repo,
run this from the agent's folder:
`cp -r claude-code-skill ~/.claude/skills/fielding-risk-advisor`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | The fielding update form |
| [output-template.md](output-template.md) | What the read looks like |
| [example.md](example.md) | Day 4 in field: healthy topline, dying quota cell |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

The last agent in the chain. Its baselines come from the
[Bid Comparator](../bid-comparator/)'s awarded bid; screener-leak suspicions
send you back to the
[Questionnaire Risk Reviewer](../questionnaire-risk-reviewer/); its
divergence log feeds reconciliation and the next project's
[Feasibility Checker](../feasibility-checker/) as fielding history.
