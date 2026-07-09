# Questionnaire Risk Reviewer

Reads your screener and survey the way fielding will: what breaks IR,
inflates LOI, stalls quotas, invites fraud, and dies on a phone. Sample and
fielding risk only — it does not judge your methodology.

## Use it in 60 seconds

1. Open [prompt.md](prompt.md) and copy everything below the line into a new
   chat in Claude, ChatGPT, or Gemini (or into a Claude Project / Custom GPT
   / Gem as instructions).
2. Paste your screener **with routing logic**, the survey, and the context —
   the [input template](input-template.md) covers it.
3. You get a six-dimension risk table, question-by-question flags with fix
   directions, an LOI reality check, and the list of things to tell your
   supplier before launch.

**Claude Code users:** copy the skill folder instead —
`cp -r claude-code-skill ~/.claude/skills/questionnaire-risk-reviewer`

## Files

| File | What it's for |
|---|---|
| [prompt.md](prompt.md) | The copy/paste prompt (start here) |
| [agent.md](agent.md) | Full spec — everything this agent does and doesn't do |
| [input-template.md](input-template.md) | What to paste, incl. routing logic |
| [output-template.md](output-template.md) | What the review looks like |
| [example.md](example.md) | A screener with the classic telegraphing flaw |
| [claude-code-skill/](claude-code-skill/) | Claude Code skill version |

## Chains with

Best run after award, before launch. Its flags sharpen the
[Feasibility Checker](../feasibility-checker/)'s IR concerns, and its
"tell your supplier" list pre-empts the conversation the
[Fielding Risk Advisor](../fielding-risk-advisor/) would otherwise have on
day 3.
