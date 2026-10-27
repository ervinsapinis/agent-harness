# harness

A Claude Code plugin that keeps the user in control of a project's decisions:

- a tiered decision protocol, with 3 genuine options plus the user's own answer;
- a ledger that records each answer once and turns it into a rule;
- a verification ladder (R1–R4);
- an independent reviewer.

The plugin holds only the process. Each project's content (rules, ledger, secret denies) lives in that project's own
layer, which the `init` skill sets up.

## Layout

| Path | What it holds |
|---|---|
| `output-styles/deliberate.md` | The always-on protocol. It switches on together with the plugin. |
| `skills/init` | Sets up a project layer. |
| `skills/decide` | Records a decision in the ledger. |
| `agents/reviewer.md` | The on-demand independent review. |
| `docs/` | Design and the harness's own decision ledger. |

## Load it

`claude --plugin-dir C:\proj\harness`

To compare runs, start a session without the flag.

## Rule

No work content in this repo: no employer or client code, names, configs or findings. Work layers stay on the work
machine.
