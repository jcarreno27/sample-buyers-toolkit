# Brief Builder

Turns messy project context — client emails, call notes, half-specs — into a
supplier-ready sample brief, with every gap and assumption made visible.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions).
2. Paste in everything you have about the project. The
   [input template](input-template.md) helps but isn't required.
3. Answer its clarifying questions (or say "just proceed"). You get a
   structured brief plus a list of gaps, contradictions, and decisions to
   make before it goes to suppliers.

**Optional — only if you use Claude Code** and would prefer to install
this agent as an auto-activating skill. Once you've downloaded the repo,
run this from the agent's folder:
`cp -r claude-code-skill ~/.claude/skills/brief-builder`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | Fill-in intake form |
| [output-template.md](output-template.md) | What the response looks like |
| [example.md](example.md) | Realistic messy-input → brief example |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

Output feeds the [Feasibility Checker](../feasibility-checker/) (gut-check the
brief) and the [RFP Drafter](../rfp-drafter/) (turn it into supplier emails).
