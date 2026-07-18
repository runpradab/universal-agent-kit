# START HERE — Company AI Workspace

This folder is a ready-to-use starter for running your company's AI
agents (accountant, market researcher, and any future ones) with the
Universal Agent Kit. It was generated from UNIVERSAL-KIT.md v2.3
following its Part 6 "domain agent" pattern.

## The one idea to understand

**Files are the memory.** Your phone, your PC, and any AI session all
read and write the same git repo. Nothing important lives in a chat
window. That's why it doesn't matter which device you're on — you
resume anywhere with prompt P4 (see below).

> **Already have a project with workflows/tasks in it?** Don't start
> fresh — follow MERGE-INTO-EXISTING.md instead of steps 2–3 below.
> It maps your existing (even scattered) files into this structure
> without losing anything.

## Setup on your PC (one time, ~15 minutes)

1. Install Claude Code: https://claude.com/claude-code
   (or use any capable AI CLI — the kit is model-agnostic)

2. Create a NEW private GitHub repo for your company workspace,
   e.g. `my-company-hq`. Do NOT work inside the kit repo — the kit
   repo stays clean as the master (kit Part 9 golden rule).

3. Copy the CONTENTS of this `company-workspace/` folder into the
   new repo, plus a copy of `UNIVERSAL-KIT.md` from the kit repo
   root. Commit and push.

4. Open a terminal in the new repo and start Claude Code. Paste:

   ```
   Read UNIVERSAL-KIT.md and CLAUDE.md. Then interview me using the
   headings of docs/company-brief.md and fill it in from my answers.
   Then read .claude/agents/accountant.md and interview me about our
   accounting setup (which accounting software, chart of accounts,
   who approves what) and fill in its "Company facts" section.
   ```

5. Drop your existing documents (expense policy, price lists, past
   research, anything agents should know) into `docs/raw/`, then run
   kit prompt P6a to compile them into the wiki.

That's it. From then on:

- **Start any session** with kit prompt P4 (resume).
- **Give work** to a specific agent: "Use the accountant agent: ..."
  or "Use the market-researcher agent: ...".
- **From your phone**, use Claude Code on the web / mobile app
  pointed at the same repo — same files, same memory.

## What's in this starter

```
CLAUDE.md                          orchestrator rules (the main session obeys this)
docs/company-brief.md              fill via interview — every agent reads it first
docs/wiki/_schema.md               wiki categories for a company (not a codebase)
docs/wiki/index.md                 wiki map (starts empty)
docs/lessons.md                    learning loop (starts empty)
docs/raw/                          drop source documents here
plans/                             agents write work plans here
.claude/agents/accountant.md       domain agent 1
.claude/agents/market-researcher.md domain agent 2
```

## Adding your next agent (HR, sales, legal, ...)

Clone one of the two agent files, change: name, description (this is
the routing signal — be specific), the domain boundaries, and the
domain Definition of Done. Add its wiki category to _schema.md.
That's the whole process — kit Part 6.
