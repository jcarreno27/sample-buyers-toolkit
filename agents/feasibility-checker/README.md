# Feasibility Checker

Pressure-tests a sample brief before suppliers see it. Rates feasibility
**risk** — Low / Medium / High per dimension, with reasoning — finds the
killer combinations, and turns every concern into a mitigation or a supplier
question. It never issues verdicts, because honest feasibility doesn't come
with certainty.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions).
2. Paste in your sample brief — the [Brief Builder](../brief-builder/)'s
   output drops straight in, or use the [input template](input-template.md).
3. Answer its clarifying questions (or say "just proceed"). You get an
   overall risk rating, a dimension-by-dimension risk table, mitigations,
   and questions to put to suppliers.

**Optional — only if you use Claude Code** and would prefer to install
this agent as an auto-activating skill. Once you've downloaded the repo,
run this from the agent's folder:
`cp -r claude-code-skill ~/.claude/skills/feasibility-checker`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | Fill-in request form |
| [output-template.md](output-template.md) | What the response looks like |
| [example.md](example.md) | Full consumer example + B2B contrast |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

Takes the [Brief Builder](../brief-builder/)'s output. Its supplier questions
paste into the [RFP Drafter](../rfp-drafter/); its risk table becomes the
checklist the [Bid Comparator](../bid-comparator/) scores supplier replies
against.
