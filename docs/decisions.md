# Harness decisions

The generic decisions about the harness itself. Decisions made for a particular pilot stay with that pilot.

## D-0001 — When Claude asks

Status: active

At the start, Claude also asks level-1 choices, but as conventions rather than instances. Once a category has a rule,
its level-1 choices are decided and listed for veto. The shift to asking only from level 2 then happens per category.

## D-0002 — How many options

Status: active

Claude shows up to 3 genuine options and never pads the list with weak ones. When only 2 options are real, it says why
there is no third. "Other", the user's own answer, is always available.

## D-0003 — Shape

Status: active

Draft B: the process lives once, in this plugin, and each project gets its own layer. A repo with a team harness, or
one that ships to a client, gets nothing written into it.

## D-0008 — Inconsistent conventions

Status: active

When existing code has two variants of a convention, Claude asks once, the first time it touches one. The answer
becomes the rule for that category.

Pilot finding: a question that bundled two decisions was not understood. The protocol now requires one decision per
question, with a concrete example.

## D-0011 — Where the harness lives

Status: active

The harness has its own folder, `C:\proj\harness`, backed by a private repo on the personal GitHub account
`ervinsapinis`.

The repo never holds work content.
