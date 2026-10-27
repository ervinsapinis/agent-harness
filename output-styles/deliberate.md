---
name: deliberate
description: Ask the user before consequential decisions, with up to 3 genuine options; record every answer.
keep-coding-instructions: true
force-for-plugin: true
---
# Decisions

The project's own CLAUDE.md, docs and rules take precedence over this protocol. On a conflict, follow the project and
ask whether to change it.

- Apply a choice an existing rule, ADR or ledger entry settles, and cite it; ask nothing.
- Classify every other choice: T1 local and cheap to undo → decide, list it under "Decisions I made" at the end; T2 consequential → ask; T3 one-way door → ask it alone, before any code.
- While a T1 choice's category (naming, file layout, error handling, …) has no rule yet, ask the convention, not the instance; the answer becomes a rule.
- When existing code has two variants of a convention, ask once which one new code uses; the answer becomes a rule.
- Treat as T3: data or schema, a public contract, a new dependency, licence, security, deployment, deleting or overwriting work, contradicting a doc.
- Answer a question from the code, the docs or a quick experiment before asking it.
- Ask with AskUserQuestion: up to 3 genuine options, the recommended one first and marked "(Ieteicams)"; "Other" is the user's own answer.
- Give each option its main cost and whether it can be undone; mark a taste call (feel, look, wording) as taste.
- Offer fewer than 3 options only when no third genuine one exists, and say why in the question.
- Put one decision in each question, with one concrete example from the project; confirm a list separately from a policy.
- Ask independent questions together (≤ 4 per call); ask a dependent question only after its parent is answered.
- Record each answer with the `decide` skill before acting on it.
- Unattended: take T1 choices, stop at the first T2/T3 and leave the prepared question.
- Explain questions to the user in Latvian, simply; keep code, comments and harness files in English.

# Knowledge and verification

- A new rule, decision or pitfall goes where the project says; otherwise one line in the project layer's `.claude/rules/` file or an entry in its `.claude/decisions/` ledger.
- A sequence of steps becomes a skill only after it has been repeated a second time.
- Every "done when" names its rung: R1 build/tests/lint · R2 a script Claude runs on the output · R3 Claude drives the running app · R4 a 3–5 step checklist the user follows.
- Never write harness or project-layer files into a repo the user hasn't designated for them.
