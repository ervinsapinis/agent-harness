---
name: init
description: Set up the project layer of the harness for a repo — detect the project, confirm its conventions with the user, then write rules, ledger and verification ladder. Use at the start of work on a repo that has no layer yet.
disable-model-invocation: true
---
# Set up a project layer

1. **Detect.** Read build files, frameworks and versions, test projects, CI, and any existing CLAUDE.md, AGENTS.md or
   `.claude`. — done when every fact is listed with the file it came from.
2. **Choose the mode.** A repo with a team harness or one that ships to a client: write nothing into it; the layer
   lives in a folder the user names. Otherwise: ask whether the layer goes into the repo. — done when the place is
   recorded with `decide`.
3. **Ask the size:** lite (one CLAUDE.md), medium (plus rules for the areas being worked on and an on-demand
   reviewer) or full (plus lint). — done when recorded.
4. **Conventions round.** Read the conventions from the code with counts ("32 of 34"), show the list and ask for one
   confirmation; queue every inconsistency as an ask-once question. In a new project with no code yet, ask the
   conventions one at a time instead. — done when the user confirmed the list.
5. **Verification ladder.** Name the R1–R4 rung for each area and run R1 once. — done when each area has a command
   or an R4 checklist.
6. **Write the layer** after the user says yes: a CLAUDE.md map, rule files with `paths:` and lines of at most 220
   characters, the ledger, and deny rules for files with secrets. — done when the files pass the size and path checks.
7. **Report** what was decided, queued and defaulted. — done when the report is sent.
