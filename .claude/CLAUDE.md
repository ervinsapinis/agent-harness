# Working on the harness

- Read `docs/status.md` first, then `docs/decisions.md`.
- Keep this repo free of work content: no employer or client names, code, configs or findings.
- Write harness files in English. Explain to the user in Latvian, simply.
- Ship each change in one commit containing:
  - the edit;
  - a `CHANGELOG.md` entry;
  - a version bump in `.claude-plugin/plugin.json`;
  - the updated `docs/status.md`.
- Commit and push only when the user asks.
- After a push, tell the user to run `claude plugin marketplace update ervinsapinis`, then
  `claude plugin update harness@ervinsapinis`.
