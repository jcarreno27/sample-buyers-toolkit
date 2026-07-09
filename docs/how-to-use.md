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
Instructions. Most agent prompts fit the ~8,000-character Instructions
limit; the Incentive Advisor runs slightly over (trim a few lines, or use
it as a first-message chat), and the **full-kit prompt is well over**
(~10k vs. ~8k), so paste the full kit as the first message of a chat. For a
persistent whole-kit setup, see **Power setup** below. Quick version for any agent, on any plan: first message of a new
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

## Power setup: turn the kit into a saved Project, Gem, or Custom GPT

If you use the kit a lot, set it up once as a saved assistant instead of
pasting a prompt each time. Two things to know first. Creating a Claude
Project or a ChatGPT Custom GPT needs a paid plan; Gemini Gems are free.
And all three keep whatever you put in the **instructions** field in view on
every message, but treat **uploaded files** as a reference library they
search only when they judge it relevant. So anything that must apply on
every turn (the router and the guardrails) belongs in the instructions
field, never in an uploaded file.

**Claude Projects or Gemini Gems:**
1. Create a Project (Claude) or a Gem (Gemini).
2. Open `full-kit/full-kit-prompt.md`, copy the prompt itself (everything
   below the `---` near the top), and paste it into the instructions field.
   Watch the character counter; if the field won't take the whole thing,
   paste the router and guardrails from the top and move the seven role
   sections into a knowledge file, then add one line telling the assistant
   to follow those role sections.
3. Recommended: upload the reference docs (`glossary.md`,
   `practitioner-benchmarks.md`, `sample-procurement-basics.md`) as
   knowledge, so the assistant can lean on your definitions and benchmarks.
   Gems allow up to 10 knowledge files.
4. Start a chat. The reliable way to summon a specialist is to name it
   ("act as the Bid Comparator"); it will also try to infer the role from
   what you paste.

**ChatGPT Custom GPTs:**
The Instructions box caps at 8,000 characters. Most single-agent prompts
fit; the full kit (about 10,000) does not. Don't work around that by putting
the whole playbook in a knowledge file: guardrails and routing placed in a
file get pulled in only when ChatGPT decides they're relevant, so they get
skipped on many turns, which is the opposite of what this kit is for.

- For one agent: paste that agent's `prompt.md` into the Instructions box.
  (If a prompt runs slightly over 8,000 characters, trim a few lines or use
  it as a first-message chat.)
- For the whole kit: the simplest reliable route is one Custom GPT per agent
  you use. If you want a single GPT for everything, keep the router and
  guardrails in the Instructions box and move the detailed role sections
  into a knowledge file, then name the role you want each time.

On all three, naming the role is the dependable path; auto-routing is a
convenience, not a guarantee. If a reply ever ignores a guardrail, name the
role explicitly, and on ChatGPT confirm the guardrails are in the
Instructions box rather than only in a file.

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
