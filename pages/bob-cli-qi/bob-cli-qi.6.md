# Bead: bob-cli-qi.6 — Passive-rendering proof, docs sweep, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.6` · **Size:** medium
**Created:** 2026-11-26 10:06:13 EST · **Closed:** 2026-11-26 15:00:06 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

## Description

finish: add the unit proof that folds and refreshes never write the vault or spawn bob from paint, and sweep the bob-plugins and bob-cli docs onto the single-owner card contract. Apply only the memory decisions answered yes, then deploy cleanly from master with the isolated post-sync smoke check.

## Notes

[2026-11-26T18:43:34Z · bob-cli-qi.6] PROPOSED FOLLOW-UP: Fix the clean-base docs-check home-path privacy false positive — npm run docs:check uses bob-cli master at 3659edc and fails at docs/snooze.md:281 on /home/bryan missing from privacy_baseline.txt; plugin docs lint and word budget pass.

[2026-11-26T19:27:27Z · bob-cli-qi.6--1] PROPOSED FOLLOW-UP: Fix the clean-base `just check` compilation failure in snooze CLI tests — `just check` fails at clean committed primary base c89ba1d4c49775b1840c065f0f31d262e60930ac with E0433 for `super::notify` and `super::receipt` in src/native/snooze/cli.rs; qi.6 changes no snooze files.

[2026-11-26T20:00:06Z · bob-cli-qi.6--5] Verification and deployment closeout:
- Isolated: `xvfb-run -a npm run smoke:obsidian -- --report /tmp/qi6-obsidian-smoke.json` — PASS, exit 0; report `/tmp/qi6-obsidian-smoke.json` had pass=true and zero failures.
- Deployed attempt: `npm run smoke:obsidian -- --deployed-vault /home/bryan/bob --report /tmp/qi6-obsidian-smoke.json` — exit 2, no X display. Retried as `xvfb-run -a npm run smoke:obsidian -- --deployed-vault /home/bryan/bob --report /tmp/qi6-obsidian-smoke.json` — exit 1 at pre-check: bob-ledger-tools sync was drift. It did not write a new report; the path still contains the prior isolated pass (mtime 2026-11-26 14:48 EST).
- Runtime: node v20.19.2; Node 22 is absent, but system `undici.WebSocket` is available and satisfies this script's fallback, so no Node prerequisite blocker was found.
- Clean sync already completed: `bob plugins sync --repo "$PWD" --no-pull` — 0 copied, 0 skipped, 34 unchanged. It warned that the bob-emoji vault folder has 4 tracked files.
- Current `bob plugins list --format json --no-pull --repo "$PWD"`: count=12, synced=11, drift=1, not_installed=0; bob-ledger-tools 1.169.0 is drifted. Current source advanced from deployed source_head f6458cb to b021aff (Ref Card kit); dry run would copy only bob-ledger-tools main.js and styles.css. This is unrelated upstream work, so it was not deployed.
- `sase bead epic-symbols bob-cli-qi.6`: no --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-qi.4](bob-cli-qi.4.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qi.5](bob-cli-qi.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qi.6.md) | [bob-cli-qi.6](bob-cli-qi.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c89ba1d`](https://github.com/bobs-org/bob-cli/commit/c89ba1d4c49775b1840c065f0f31d262e60930ac) | docs(bank): establish path-canonical single-owner hub | [bob-cli-qi.6](bob-cli-qi.6.md) | 2026-11-26 13:57:29 EST |
| bob-plugins | [`bob-plugins@17a0567`](https://github.com/bobs-org/bob-plugins/commit/17a0567013d75cecd1f8c9751993864151cf524e) | docs(props): document home-card ownership and passive rendering | [bob-cli-qi.6](bob-cli-qi.6.md) | 2026-11-26 14:21:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.2][1] | Need the active phase scope to determine whether the bank props failure belongs in its discovery note | 1 |
| read-by | [agent:research.6k.cld][2] | Check qi.6 dependencies for card sequencing | 2 |
| read-by | [agent:research.6k.gem][3] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |
| read-by | [agent:research.6l.gem][4] | Check live progress of active property-card and prose epics for parallelization analysis | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qj.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6k.gem/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
