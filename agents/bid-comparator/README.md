# Bid Comparator

Takes pasted supplier replies — however differently formatted — and produces
a normalized side-by-side comparison: price, assumptions, adjustment clauses,
feasibility claims, quality terms, and what each bid is *silent* about. It
frames the award decision; it never makes it.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions).
2. Paste your spec and each supplier reply between markers — the
   [input template](input-template.md) shows the format. Alias supplier
   names if you prefer.
3. You get a comparison table (gaps marked NOT STATED), a plain-English
   "are these prices even comparable?" analysis, a risk read per bid, and
   pre-award questions for each supplier.

**Optional — only if you use Claude Code** and would prefer to install
this agent as an auto-activating skill. Once you've downloaded the repo,
run this from the agent's folder:
`cp -r claude-code-skill ~/.claude/skills/bid-comparator`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | Paste format for supplier replies |
| [output-template.md](output-template.md) | What the response looks like |
| [example.md](example.md) | Three fictional bids — including a cheap one with a catch |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

Want a spreadsheet? The kit-wide
[supplier-comparison-grid.csv](../../templates/supplier-comparison-grid.csv)
mirrors the comparison table and adds a few extra rows for note-keeping.

## Chains with

Works best on replies to the [RFP Drafter](../rfp-drafter/)'s emails (same
numbered items across suppliers = clean extraction). The winning bid's
assumptions become the baselines the
[Fielding Risk Advisor](../fielding-risk-advisor/) tracks against.
