# Sample Buyers Toolkit

**A free, modular kit of AI agents for market researchers who buy sample.**

These are plain prompt files. No app, no code, nothing new to sign up for,
no setup beyond copying text. Paste one into Claude, ChatGPT, Gemini, or any capable LLM and
you have a specialist for one job in the sample-buying process. Use one
agent, a few, or the whole team.

## What this kit doesn't do (read this first)

- **No CPI or price predictions.** Real prices come from suppliers quoting
  real specs. The agents discuss cost drivers and direction, never numbers.
- **No feasibility guarantees.** You get risk (Low/Medium/High with
  reasoning), because honest feasibility doesn't come with certainty.
- **No claims about specific suppliers.** The agents know only what you
  paste in.
- **No replacement for anyone.** Not your sample providers, not your PMs,
  not your judgment. This kit makes an experienced buyer faster and a newer
  buyer harder to fool. That's the whole promise.

Full honesty page: [limitations-and-guardrails](docs/limitations-and-guardrails.md).

## The seven agents

One per stage of the sample-buying lifecycle, plus a cross-cutting
incentive specialist:

| Stage | Agent | One job |
|---|---|---|
| 1 | [Brief Builder](agents/brief-builder/) | Messy context → supplier-ready sample brief |
| 2 | [Feasibility Checker](agents/feasibility-checker/) | Brief → feasibility *risk* assessment, mitigations, supplier questions |
| 3 | [RFP Drafter](agents/rfp-drafter/) | Brief → supplier RFP emails (detailed, short, follow-ups) |
| 4 | [Bid Comparator](agents/bid-comparator/) | Pasted supplier replies → honest side-by-side, hidden risk lit up |
| 5 | [Questionnaire Risk Reviewer](agents/questionnaire-risk-reviewer/) | Screener/survey → fielding-risk review (IR, LOI, quotas, mobile, fraud) |
| 6 | [Fielding Risk Advisor](agents/fielding-risk-advisor/) | In-field updates → trajectory risk + decide-now / ask-supplier / watch |
| ✳ | [Incentive Advisor](agents/incentive-advisor/) | What to pay respondents: opportunity-cost anchored, tiered, honest about its calibration |

Each agent is swappable and standalone. Prefer one assistant for the whole
lifecycle? The [full kit](full-kit/) bundles all seven behind a router.

## Start in 60 seconds

1. Pick an agent from the table (or the
   [selection guide](docs/agent-selection-guide.md)).
2. Open its `prompt.md`, copy everything below the horizontal line.
3. Paste it into a new chat, or better, into a Claude Project / Custom
   GPT / Gemini Gem so it persists.
4. Paste in your project material. Answer its questions or say "just
   proceed."

Details per platform (including the optional Claude Code skill versions):
[docs/how-to-use.md](docs/how-to-use.md).

## What's in the repo

```
agents/            seven standalone agents, each with prompt, spec,
                   input/output templates, worked example, Claude Code skill
full-kit/          all seven in one prompt, plus the workflow map
templates/         fill-in forms: intake, RFP, bid pasting, fielding
                   updates, questionnaire review, comparison grid (CSV)
docs/              how-to-use, agent selection, a full worked project,
                   benchmark customization, procurement basics,
                   limitations, privacy, glossary
```

The best tour: [one fictional project run start to finish](docs/full-workflow-example.md).

## Make it yours

The agents ship with general industry heuristics, plus
[docs/practitioner-benchmarks.md](docs/practitioner-benchmarks.md), a set
of field-tested starting values from my fourteen years on the supplier
side (funnel mechanics, panel overlap, timeline saturation, LOI decay,
incentive logic). Every prompt has a **"Your benchmarks"** section. Paste
those in, then overwrite them with your own IR observations, LOI rules,
and required terms as they accumulate.
How: [docs/customizing-your-benchmarks.md](docs/customizing-your-benchmarks.md).

Before pasting supplier replies or client material anywhere, read
[docs/privacy-and-data-use.md](docs/privacy-and-data-use.md). It's short
and it matters.

## Why I built this

I'm Jeremy Carreno. I've spent fourteen years on the *other* side of your
RFPs, selling sample. From that seat you see exactly how buyers get hurt:
the optimistic IR nobody questioned, the bids that were never comparable,
the screener that telegraphed its quals, the quota cell that died quietly
on day 4. Most of what goes wrong in sample procurement is catchable early,
and most of the catching is a checklist wearing a judgment costume. That's
a job language models are genuinely good at, but only *if* they're constrained from
faking the certainty this industry already has too much of. Hence the
guardrails, which are the point of this kit as much as the prompts are.
This kit is me writing down what I'd want every buyer across the table to
ask.

It's free, MIT-licensed, and I'd genuinely like it to get better.
[Contributions welcome](CONTRIBUTING.md).

## Roadmap (contributions welcome)

Candidate future agents: CPI Pressure Checker · Supplier PM Advisor ·
Client Update Writer · Data Quality Risk Reviewer · Supplier Memory Agent.
(Incentive Advisor graduated from this list in 1.1.0.) The bar for adding
one: a single sentence should describe its one job, and it must pass the
[guardrail canon](CONTRIBUTING.md).

## License

[MIT](LICENSE). Use it, fork it, bring it to work.
