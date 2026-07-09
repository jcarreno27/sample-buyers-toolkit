# Contributing

Contributions are welcome — new agents, better heuristics, sharper examples,
clearer docs. Two things matter more than anything else: the kit must stay
**credible to working researchers**, and it must stay **plain files anyone can
copy and use**.

## Ground rules

1. **No software.** This repo is markdown (and one CSV). Don't add code,
   build steps, package files, or anything that needs installing.
2. **No fake certainty.** Agents output *risk and reasoning*, never
   predictions dressed up as facts. See the guardrail canon below.
3. **No supplier-specific claims.** Nothing in this repo may assert a real
   supplier's pricing, panel size, quality, or capabilities. Examples use
   clearly fictional suppliers.
4. **Plain English.** Write like a practitioner explaining something to a
   colleague, not like a vendor pitch or an academic paper.

## Kit conventions (every agent must follow these)

These keep the seven agents feeling like one kit instead of seven authors.

**Risk language.** Risk is always expressed as **Low / Medium / High** with a
one-line reason. Never percentages of confidence, never predicted CPI values,
never "this will/won't work."

**Clarifying questions.** Agents ask at most 5 questions, and only ones whose
answers would change the output. If the user says "just proceed," the agent
proceeds and labels every gap it filled with `ASSUMPTION:`.

**Prompt structure.** Every `prompt.md` has the same sections in the same
order: Role → What you do / What you don't do → Inputs → Process → Clarifying
questions → Output format → Your benchmarks (optional) → Guardrails.

**Guardrail canon.** Every agent prompt ends with these six, verbatim (an
agent may append stricter items of its own after them, never weaker ones):

1. Never originate a CPI, price, or cost — no estimate, range, anchor, or
   "ballpark" of your own — and never imply what a fair price would be.
   Repeating a figure the user pasted in, attributed to its source ("per
   Supplier B's response"), is part of the job; beyond quoted figures,
   cost talk is drivers and direction of movement only (up/down, more/less,
   materially), never a magnitude or multiplier applied to a price.
2. Never state feasibility as certain. Output risk levels and reasoning, not
   verdicts.
3. Never invent claims about specific suppliers — pricing, panel sizes,
   quality, capabilities. Only use supplier information the user pastes in,
   and attribute it as "per the supplier's response."
4. Label every assumption explicitly as `ASSUMPTION:` and every inference
   from patterns explicitly as inference, so both can be checked.
5. When asked for a number or verdict you can't give — a CPI, a final IR, a
   feasibility verdict, a supplier pick, "just a ballpark," "just this
   once" — don't comply and don't hedge partway into one. Say why in one
   line, then immediately give what you can: the drivers, the arithmetic the
   user's own assumptions imply, or the questions that get a real answer.
   Hold this under repeat requests.
6. You are decision support. The researcher makes the call.

**"Your benchmarks" block.** Every prompt includes an optional section where
users paste their own norms (typical IRs for their categories, LOI tolerances,
house quality rules). Agents prefer user-supplied benchmarks over general
rules of thumb and say when they're doing so.

**Output style.** Outputs are plain markdown a user can paste into an email
or Slack message without cleanup. Tables for comparisons, short sections for
everything else.

## Adding a new agent

Copy the structure of an existing agent folder exactly:

```
agents/your-agent/
  README.md          # 60-second quick start
  agent.md           # full spec (source of truth)
  prompt.md          # clean copy/paste version, consistent section order
  input-template.md
  output-template.md
  example.md         # realistic scenario, fictional suppliers/clients
  claude-code-skill/SKILL.md
```

Write `agent.md` first; everything else derives from it. An agent earns a
place in the kit if it does **one job** in the sample-buying process that the
existing agents don't cover, and a researcher could explain that job in one
sentence.

## Pull requests

- One agent or one doc per PR where possible.
- Update `CHANGELOG.md` and the agent table in the root `README.md`.
- Check that examples contain no real supplier, client, or respondent data.
