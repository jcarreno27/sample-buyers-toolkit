# Limitations and guardrails

Read this before trusting the kit with anything that matters. The agents
are useful precisely *because* they refuse to do certain things; this page
is the honest list.

## What the agents will not do — by design

**Predict CPIs or prices.** A real CPI is a supplier quoting a real spec at
a real moment, against their actual panel and current demand. Any tool that
"predicts" your CPI without that is making it up. The agents discuss cost
*drivers* and *direction* — "halving IR pushes cost up materially" — never
"expect $9.50."

**Certify feasibility.** Feasibility depends on actual IR, panel
composition that week, competing studies, and screener behavior in the
wild. Nobody knows these in advance — including suppliers, including these
agents. You get risk levels with reasoning. If you need someone to say
"this will work," that someone doesn't honestly exist.

**Make claims about specific suppliers.** The agents know nothing about any
real supplier's pricing, panel size, quality, or capabilities, and are
instructed never to pretend otherwise. Everything they say about a supplier
comes from what *you* pasted in, attributed as "per the supplier's
response."

**Make your decisions.** The Bid Comparator won't pick a winner; the
Fielding Risk Advisor won't tell you to pull the plug. They frame decisions
and name costs. The judgment — and the accountability — stays with you.

## Real limitations — not by design, just true

**They're language models.** They can misread a pasted table, mangle
arithmetic, or state something confidently that's wrong. Check any number
that feeds a decision — especially totals, quota math, and anything you'd
repeat to a client. The output formats deliberately show reasoning so you
*can* check it.

**Their general heuristics are general.** "LOI over 20 minutes on consumer
mobile is risky" is a fine rule of thumb and wrong for someone's specific
panel. Your own benchmarks beat the defaults — feed them in
([how](customizing-your-benchmarks.md)).

**They don't know today's market.** Panel capacities, seasonal effects,
current fraud patterns, what happened in fielding last week — invisible to
them unless you paste it in.

**Quality varies with the underlying model.** The same prompt runs sharper
on a stronger model. If an output seems shallow, that's the first variable
to check.

**They're built for quantitative online sample.** Qual recruiting, CATI,
in-person, and panel *management* are adjacent worlds — the structure may
help, but the heuristics weren't written for them.

## If an agent breaks its own rules

Prompts steer; they don't guarantee. If an agent quotes you a CPI, declares
a project feasible, or "recalls" something about a named supplier you never
pasted, treat that output as wrong, and remind it of its guardrails (that
usually fixes the session). If you can reproduce it, file an issue —
guardrail leaks are treated as bugs here.

## The one-sentence version

These agents make an experienced buyer faster and a newer buyer harder to
fool — they replace **no part** of supplier expertise, PM craft, or your
judgment.
