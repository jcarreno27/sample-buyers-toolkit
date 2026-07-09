# How to use this kit

No installation, no code, and nothing new to sign up for. Every agent is a
text file you copy into an AI chat tool you already use. Total setup time:
about a minute.

## Step 1 — Get the files

**Easiest (no GitHub knowledge needed):** on the repo page, click the green
**Code** button → **Download ZIP** → unzip. You now have every agent.

**Just one agent:** open the agent's folder on GitHub → open `prompt.md` →
click the **Raw** button → select all, copy. That's the whole download.

**Git users:** `git clone` as usual.

## Step 2 — Install an agent (pick your tool)

The same `prompt.md` works everywhere. Copy everything **below the
horizontal line** in the file.

### Claude (claude.ai)
Best: create a **Project** → paste the prompt into the project's
instructions. Every chat in that project is the agent. Quick version: paste
the prompt as the first message of a new chat.

### ChatGPT
Best (creating Custom GPTs requires a paid ChatGPT plan): create a
**Custom GPT** (Explore GPTs → Create) → paste the prompt into its
Instructions. Every standalone agent fits within the instruction
limit; the **full-kit prompt does not** (~10k characters vs. a ~8k cap) —
for the full kit in ChatGPT, paste it as the first message of a chat
instead. Quick version for any agent, on any plan: first message of a new
chat.

### Gemini
Best: create a **Gem** → paste the prompt as its instructions. Quick
version: first message of a new chat.

### Any other LLM (Copilot, local models, etc.)
Paste the prompt as the first message, or as the system prompt if the tool
exposes one. The prompts assume nothing tool-specific.

### Claude Code (optional, for those who use it)
Each agent ships a skill version. First download the repo (Download ZIP or
`git clone`) — the command below copies the skill from those local files;
it doesn't fetch anything from GitHub. From the repo's root folder, run:

```
cp -r agents/<agent-name>/claude-code-skill ~/.claude/skills/<agent-name>
```

e.g. `cp -r agents/brief-builder/claude-code-skill ~/.claude/skills/brief-builder`.
Then just describe the task in Claude Code ("compare these three bids") —
the skill activates. Bonus: skills can read files in your working folder,
so you can point them at saved RFP replies instead of pasting.

Installing several agents doesn't wire them together — there's no automatic
pipeline. Each agent still takes whatever you give it as input. What one
Claude Code conversation *does* give you is continuity: ask it to "build a
brief, then feasibility-check it" and the brief it just made is right there
for the next step — because the conversation carries the context, not
because the skills hand off to each other.

## Step 3 — Use it

1. Paste in your material. Each agent's `input-template.md` shows the ideal
   shape, but rough material works — that's the point.
2. Answer its clarifying questions, or say **"just proceed"** and it will
   continue with labeled assumptions.
3. Get plain-markdown output you can paste into an email or Slack.

## One agent or the whole team?

- Only ever compare bids? Install just the [Bid Comparator](../agents/bid-comparator/).
- Want one assistant across a project's life? Install the
  [full kit](../full-kit/) — it routes between all seven roles.
- Not sure? Read the [agent selection guide](agent-selection-guide.md).

## Three habits that make the agents much better

1. **Give real numbers.** "IR feels low" gets generic advice; "IR reading
   7% against a bought 10%" gets a real answer.
2. **Fill in "Your benchmarks."** Every prompt has a section for your own
   norms — see [customizing-your-benchmarks.md](customizing-your-benchmarks.md).
3. **Strip what shouldn't leave the building** before pasting — see
   [privacy-and-data-use.md](privacy-and-data-use.md).

## What these agents will refuse to do

Predict CPIs (even "ballpark" ranges), certify feasibility, or make claims
about specific suppliers you haven't pasted in. That's by design — see
[limitations-and-guardrails.md](limitations-and-guardrails.md). If an agent
ever does one of those things anyway, treat that output as wrong.
