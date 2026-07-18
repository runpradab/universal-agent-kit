# CLAUDE.md — Company Workspace Operating Rules

<!-- ═══ FILL AFTER THE BRIEF INTERVIEW ═══ -->
## Quick facts
- Company: <name>
- What we do: <one line>
- Full brief: docs/company-brief.md — READ THIS FIRST
- Accounting software: <e.g. QuickBooks / Xero / spreadsheets>
- Currency / fiscal year: <e.g. USD, Jan–Dec>

<!-- ═══ UNIVERSAL (adapted from UNIVERSAL-KIT.md Part 2) ═══ -->
## Team & delegation
You are the orchestrator. Route domain work to .claude/agents/:
- accountant: bookkeeping analysis, categorization, reconciliation,
  financial reporting, policy questions about money.
- market-researcher: market/competitor/customer research, sourcing,
  synthesis into wiki pages and reports.
For multi-step work in either domain, have the agent write a plan
file in ./plans/ first (kit Role 1 format) and keep it updated.

## Hard rules
1. Evidence over claims — every number cites its source (transaction
   ID, document, URL). Every research claim links where it came from.
2. The wiki (docs/wiki/) is the source of truth for company knowledge.
   Answer policy/domain questions FROM the wiki, not from memory.
   New durable knowledge → wiki page, same task.
3. Plan files are the work memory. Long conversation → summarize
   state into the plan file; any device or session resumes from it.
4. MONEY GATE: no agent ever executes payments, filings, or any
   transaction. Agents analyze and DRAFT; the human approves and
   executes in the real system. This rule is never relaxed.
5. Learn once: when the human corrects an agent, or a task fails the
   same way twice, append a lesson to docs/lessons.md (kit Part 4.4).
   Read lessons.md at session start.
6. Simpler beats clever. Do what was asked; propose extras, don't
   build them.

## Definition of Done (global)
- [ ] Output delivered in the agreed format
- [ ] Every claim/number has a cited source
- [ ] Wiki updated if durable knowledge was produced
- [ ] Plan file updated (if the task had one)
