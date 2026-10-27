# Status

Where the harness stands and what comes next. Update this file in the same commit as any change.

## Now
- Version 0.1.0:
  - the always-on protocol (`output-styles/deliberate.md`);
  - `init`;
  - `decide`;
  - `reviewer`.
- A first setup pilot ran on a work repo. Its project layer and findings stay on the work machine.
- Not yet tested:
  - installing through the marketplace;
  - whether the output style switches on with the plugin;
  - whether a fresh session follows the protocol.

## Next
1. **Pilot: Pocket Factory.** Own code, so the fewest outside factors.
   - Install with `--scope local` and start with `docs/start-existing-project.md`.
   - Do one small task twice: with the plugin and without it.
2. **Fix the findings from pilot 1.**
3. **Write the `grill` skill.** It walks a plan's design tree upstream first, asks about 15 questions per session, and
   ends with a decision map.
4. **Pilot: the Bannerlord mod.** A closed engine, checked only in-game.
5. **Pilot: the news project**, using its current version.
6. **After the pilots:**
   - packs for game and game-mod;
   - `capture`;
   - a harness lint script;
   - hooks, only for rules Claude skips.

## Open questions
- **Audience:** personal only, or shareable later?
- **Budget on a Pro plan:** should a lite or medium layer be the default, and which models should subagents pin?
- **Ledger format:** one file per project (current) or one per area?
- **Unattended runs:** stop at the first T2 decision, or prepare all questions first?
- **Root file:** AGENTS.md as the root, so that other agents can use the layers?

## Findings inbox
Paste each pilot's "Harness atradumi" here as one line each: project, finding, proposed fix. When a finding is fixed,
move it to `CHANGELOG.md`.
