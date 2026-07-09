# Customizing your benchmarks

Out of the box, the agents reason from **general, publicly known industry
heuristics** — rules of thumb about IR, LOI, quotas, and timelines that any
experienced buyer would recognize. That makes them useful on day one and
honest by default.

But your own numbers are better than anyone's rules of thumb. Every
`prompt.md` includes this section:

```
## Your benchmarks (optional)

[User: paste your benchmarks here, or delete this section.]
```

Whatever you put there, the agent prefers over its general heuristics — and
it will tell you when it's doing so.

## A starter set, free

Don't have your own numbers yet? The kit ships with
[practitioner-benchmarks.md](practitioner-benchmarks.md) — field-tested
starting values from the author's fourteen years on the supplier side
(funnel mechanics, panel overlap, timeline saturation, LOI decay, screener
pass-rate bands, incentive logic). Paste any section of it into a
benchmarks block, then overwrite it with your own observations as they
accumulate.

## What to put in

Only things **you know from your own work**. Examples:

```
## Your benchmarks (optional)

- New-parent audiences, US gen-pop panels: we've seen IR 12–18% across
  6 studies (2024–2026).
- Our house LOI ceiling for consumer mobile is 18 min; anything longer
  needs sign-off.
- German B2B fields ~40% slower than US B2B for us, same spec.
- We require: day-1 soft launch at 10%, IR-adjustment clauses bounded
  in writing, supplier pays for quality removals. Treat any bid missing
  these as a flag.
- Category IR reality-check: ~8% of US children have a diagnosed food
  allergy (we use this over client guesses).
```

Good benchmarks are dated, sourced ("across 6 studies"), and specific.
"IR is usually low" is not a benchmark; "12–18% across 6 studies since
2024" is.

## What NOT to put in

- **Confidential supplier terms** — pasting Supplier X's rate card into a
  chat tool may violate your NDA. See
  [privacy-and-data-use.md](privacy-and-data-use.md).
- **Client-identifying data** — alias it.
- **Wishes.** A benchmark is what you've *observed*, not what you hope. If
  you feed the agents optimistic numbers, you've rebuilt the exact failure
  mode this kit exists to catch.

## Keeping a house benchmarks file

The habit that compounds: keep one `my-benchmarks.md` file, append to it at
every project close-out (the Fielding Risk Advisor's actuals-vs-bought
table is purpose-built for this), and paste it into any agent you use. Six
months in, you'll have the thing no general-purpose kit can ship: *your*
numbers.

Where to keep it: anywhere you keep notes. It's deliberately just a text
file. (If you use Claude Projects / Custom GPTs / Gems, paste it into the
instructions once alongside the agent prompt and update it occasionally.)
