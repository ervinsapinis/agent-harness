---
name: decide
description: Record a decision in the project ledger. Use right after the user answers a T2 or T3 question, or when the user asks to log a decision.
---
# Record a decision

1. **Find the ledger:** `.claude/decisions/<project>.md` in the project layer; create it with a one-line purpose if it
   is missing. — done when the path is known.
2. **Pick the id:** the next number after the last entry. — done when the id is unique in the file.
3. **Write the entry:** `## <id> — <decision in a few words>`, a line `Tier · Status · Area`, then `### Question`,
   `### Options` (each with its main cost and whether it can be undone), `### Answer` (the user's own words when they
   wrote any) and `### Consequences`. — done when every option the user saw is in the entry.
4. **Turn it into a rule** when the answer generalises: one positive line of at most 220 characters in the matching
   `.claude/rules/` file, and name that line under Consequences. — done when the rule exists or "no rule" is stated.
5. **Supersede, never delete:** a changed decision gets a new entry, and the old one's status becomes
   `superseded by <id>`. — done when both entries point at each other.
