# Session Handoff — context from the founding session (2026-07-18)

> Purpose: any Claude session (or other model) that reads this file
> has the full context of the phone session that created this starter,
> including the REASONING — not just the instructions. Read this
> before executing the merge. This is the kit's "files are the
> memory" principle applied to the session itself.

## Who the human is and what they want

- Solo operator running a company; works from phone (Claude Code web
  sessions) AND a PC (Claude Code terminal). Both must share one
  memory — that memory is git, never a chat window.
- Goal: a systematic AI agent team for company operations. First two
  agents: **accountant** and **market-researcher**. More roles (the
  human said "things like that") will follow — the starter is built
  so adding a role = cloning an agent file (kit Part 6).
- On the PC there is an EXISTING project with workflows and tasks
  that already work but are SCATTERED. The human explicitly chose:
  **integrate with them or replace them to be more systematic** —
  i.e. merge, preserving what works; do not blindly wipe.

## Decisions made in the founding session (with reasoning)

1. **Company workspace lives in its OWN repo, not the kit repo.**
   The kit repo stays the clean master (kit Part 9 golden rule).
   This starter folder gets copied out into the working project.
2. **Accountant is analysis-and-draft only — hard MONEY GATE.**
   It never executes payments/filings/transactions; permissions
   should be enforced at the credential level (read-only API keys)
   when real accounting-system access is wired up, because a prompt
   rule alone can be argued around. Rollout order: (1) read/analyze,
   (2) draft-with-approval, (3) never autonomous money movement.
3. **Market-researcher must cite source URL + date on every fact**,
   separate facts from interpretation, and write durable findings
   into wiki pages (competitors/, markets/) — research without
   sources or dates was judged worthless.
4. **Merge strategy for the scattered PC project** (see
   MERGE-INTO-EXISTING.md): kit structure = skeleton; existing
   content mapped in (procedures → wiki processes/, in-flight work →
   plans/, notes → docs/raw/ then compiled); inventory and full plan
   shown BEFORE any writes; explicit KEEP/MOVE/DELETE list; git
   snapshot branch first. The human should be ruthless on the DELETE
   list once content is truly migrated — half-kept duplicates
   recreate the scatter.
5. **Wiki categories chosen for a company (not a codebase):**
   finance/, policies/, vendors/, markets/, competitors/,
   customers/, processes/ — defined in docs/wiki/_schema.md.

## State when this file was written

- Branch `claude/accountant-ai-agent-9liywo` on the kit repo contains
  the complete starter (README-START-HERE.md lists the layout) and
  MERGE-INTO-EXISTING.md. Nothing on the kit's `main` was touched.
- Not yet done (waiting on the human, at the PC):
  1. Copy starter + UNIVERSAL-KIT.md into the existing PC project.
  2. Run the merge per MERGE-INTO-EXISTING.md (snapshot → inventory
     → plan → approval → execute → P6a wiki compile → P4 summary).
  3. Interview the human to fill docs/company-brief.md and the
     accountant agent's "Company facts" (accounting software still
     unknown — ASK; it determines how ledger access gets wired).
  4. Merge this branch into the kit repo's main (or open a PR) once
     the human is satisfied with the starter.

## Standing instructions to the session reading this

- Follow UNIVERSAL-KIT.md as the operating manual; PRINCIPLES
  (Part 0) are the tiebreaker. Honest counsel over agreement.
- Do the merge as a PLANNED, gated task — think first, show the
  plan, wait for approval. That is what the human meant by "think
  and merge perfectly": inventory before action, reasoning visible,
  nothing silent.
- After the merge, delete this file's "State" section or update it —
  a stale handoff is worse than none. Log lessons per kit Part 4.4.
