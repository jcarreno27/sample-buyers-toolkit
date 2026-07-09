# The full workflow — when to use which agent

Six of the seven agents map to the six stages of buying sample; you can
enter at any stage, and each agent's output is the next one's input. The
seventh — the **Incentive Advisor** — is cross-cutting: consult it after
the feasibility check and before the RFP (state the intended incentive and
bids come back comparable), and again whenever a bid's CPI sits
suspiciously close to what the respondent would need to receive, or
someone proposes "just raise the incentive" mid-field.

```
 stage 1          stage 2            stage 3        stage 4
 Brief    ──►     Feasibility  ──►   RFP      ──►   Bid
 Builder          Checker            Drafter        Comparator
    │                │                  ▲               │
    │  brief         │ supplier         │               │ awarded bid's
    │                │ questions ───────┘               │ assumptions
    ▼                ▼                                  ▼
                  stage 5                            stage 6
                  Questionnaire  ──────────────►     Fielding
                  Risk Reviewer   flags to           Risk Advisor
                                  supplier           (daily pulse)
```

## Stage by stage

**1. Brief Builder** — when a project exists as emails and call notes.
Out: a supplier-ready brief with gaps and assumptions made visible.
*Skip if:* your brief is already clean.

**2. Feasibility Checker** — when the brief exists and money hasn't moved.
Out: risk table, mitigations, and questions to put to suppliers.
*Skip if:* it's an audience you field routinely — though the IR-basis check
is cheap insurance even then.

**3. RFP Drafter** — when you're ready to ask for quotes. Feed it the brief
*plus* the Feasibility Checker's supplier questions.
Out: detailed RFP, short RFP, follow-ups, before-you-send checklist.

**4. Bid Comparator** — when replies are in. Paste them raw.
Out: normalized table, "are these prices comparable?", risk per bid,
decision framing, pre-award questions.

**5. Questionnaire Risk Reviewer** — after award, before launch (earlier if
the instrument exists earlier — cheaper still).
Out: six-dimension risk table, question flags with fix directions, the one
change that matters most, what to tell your supplier.

**6. Fielding Risk Advisor** — from soft launch to close, every day or two.
Out: trajectory read, actuals vs. bought assumptions, decide-now items,
supplier questions with numbers in them.

## The connective tissue

Three artifacts carry the whole chain:

1. **The brief** (stage 1) — quoted against in stage 3, pressure-tested in
   stage 2, the reference for "what we asked for" ever after.
2. **The awarded bid's assumptions** (stage 4) — IR, LOI, pace, terms.
   These become the baselines stage 6 measures reality against.
3. **The divergence log** (stage 6) — what actually happened vs. what was
   bought. Feed it to reconciliation, and to stage 2 of your *next* project
   as fielding history. This is how the kit gets smarter for you over time.

## Full kit vs. individual agents

- **One long-running assistant across a project** → use
  [full-kit-prompt.md](full-kit-prompt.md) (it routes between roles).
- **One job, done sharply** → use the standalone agent in
  [/agents/](../agents/) — each standalone prompt carries more depth for
  its stage than the full kit can.
- A complete worked pass of all six stages on one project:
  [docs/full-workflow-example.md](../docs/full-workflow-example.md).
