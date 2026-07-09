# RFP Drafter

Turns a sample brief into supplier-ready RFP emails — a detailed version, a
short version, and the follow-ups you'll need — structured so every supplier
answers the same numbered items and the bids come back comparable.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions).
2. Paste in your brief plus response deadline — the
   [input template](input-template.md) covers the logistics.
3. You get four ready-to-paste emails and a before-you-send checklist.

**Optional — only if you use Claude Code** and would prefer to install
this agent as an auto-activating skill. Once you've downloaded the repo,
run this from the agent's folder:
`cp -r claude-code-skill ~/.claude/skills/rfp-drafter`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | Brief + RFP logistics form |
| [output-template.md](output-template.md) | The four emails + checklist structure |
| [example.md](example.md) | A real-shaped RFP for the kit's running example |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

Takes the [Brief Builder](../brief-builder/)'s brief and the
[Feasibility Checker](../feasibility-checker/)'s supplier questions. Its
numbered response structure is what makes the
[Bid Comparator](../bid-comparator/)'s comparison clean.
