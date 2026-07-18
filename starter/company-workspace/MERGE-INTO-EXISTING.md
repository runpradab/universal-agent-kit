# Merging into an EXISTING project (scattered workflows/tasks)

Use this path instead of README step 3 when your PC project already
has workflows, task lists, notes, or agent files — even messy ones.
This adapts kit prompt P2 (UNIVERSAL-KIT.md Part 5) from code
projects to a company workspace.

## The rule

NEVER delete-and-replace blindly. Your scattered files contain real
domain knowledge (how you actually work, decisions already made,
data already gathered). The merge keeps ALL of that and only changes
WHERE it lives and HOW it's organized:

- kit structure = the skeleton (CLAUDE.md, agents, wiki, plans, lessons)
- your existing content = the organs, mapped into that skeleton
- nothing is written or deleted until you approve a file-by-file plan

## Setup

1. Copy this starter's contents + UNIVERSAL-KIT.md into your existing
   project (don't overwrite anything of yours yet — if a filename
   collides, e.g. you already have a CLAUDE.md, keep yours and name
   the starter's `CLAUDE.md.kit` for the merge to reconcile).
2. Commit your project as-is first, on a new branch:
   `git checkout -b kit-merge && git add -A && git commit -m "pre-merge snapshot"`
   (If the project isn't a git repo yet: `git init` first. The
   snapshot is your undo button.)

## The merge prompt (paste into Claude Code in the project root)

```
Read UNIVERSAL-KIT.md fully, then MERGE-INTO-EXISTING.md, then
explore this project's existing files: any workflows, task lists,
agent/prompt files, notes, and documents. Build an inventory first —
list every existing file with one line on what it contains.

Then produce a MERGE PLAN — do not write or delete anything yet:

1. STRUCTURE: the starter's layout (CLAUDE.md, .claude/agents/,
   docs/wiki/, docs/raw/, docs/lessons.md, plans/) becomes the
   skeleton.
2. WORKFLOW MAPPING: map each of my existing workflows/tasks to its
   new home —
   - repeatable procedures → docs/wiki/processes/ (one page each)
   - in-flight or recurring work → plans/ files in the kit's plan
     format, with current progress marked [x]/[ ]
   - reference material and raw notes → docs/raw/ (to be compiled
     into the wiki with prompt P6a afterwards)
   - prompt/agent definitions → rebuilt on the starter's agent bases
     (accountant, market-researcher), preserving ALL their
     project-specific instructions; propose a NEW agent file only if
     something fits neither.
3. CONFLICTS: where my existing way of working contradicts a kit
   rule, the kit wins by default — but LIST every conflict for me to
   decide, don't resolve silently.
4. DELETIONS: list files that become redundant after mapping. Mark
   each KEEP / MOVE / DELETE. Nothing is deleted without appearing
   on this list.

Show me the full plan (inventory → mapping → conflicts → deletions)
and WAIT for my approval before touching anything. After I approve,
execute it, then run prompt P6a to compile docs/raw/ into the wiki,
and finish with prompt P4 so I see the resulting state summary.
```

## After the merge

- Run kit prompt P4 at the start of every session — it reads the
  brief, wiki index, lessons, and latest plan, so any device or
  model resumes exactly where you left off.
- Scattered never comes back if you keep the two memory rules:
  work state → plan files; durable knowledge → wiki pages.
