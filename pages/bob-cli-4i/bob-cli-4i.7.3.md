# Bead: bob-cli-4i.7.3 — Contract-exact ledger lines, clean task text, one vault walk, and execute tests

[Bead Pages](../README.md) / [bob-cli-4i.7](bob-cli-4i.7.md) / bob-cli-4i.7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-4i.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-4i.land.md) · **Assignee:** `bob-cli-4i.7.3` · **Size:** medium
**Created:** 2026-10-05 18:10:31 EDT · **Closed:** 2026-10-05 18:46:20 EDT
**Plan:** [202610/bang\_task\_complete\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete_finish.md)

## Description

ledger_output: in bob-cli, report `struck_in` and `dropped` ledger entries plus a clean `task_complete.text`, print the contract's ledger lines, use the configured global filter, build the recovery vault walk once per batch, drop the dead preimage rechecks, fix new clippy warnings in the epic's files, fill the execute CLI test gaps with exact human output, and rewrite the docs/capture.md `!` execution docs.

## Notes

[2026-10-05T22:46:10Z · bob-cli-4i.7.3] Sandbox check (fixture-vault copy, NO_COLOR=1): strike printed "✓ completed [*] → [x] Fix flaky gkeep test  sase.md ^fix-flaky" + "ledger  Task Link struck in CAPTURE · 20261005.md"; dedupe printed "✓ completed [*] → [x] Carried  sase.md ^carry" + "ledger  Task Link already in MORNING; dropped the SASE copy · removed empty SASE · 20261005.md". Both match the contract.

[2026-10-05T22:46:20Z · bob-cli-4i.7.3] ledger_output done: struck_in/dropped + text in JSON, contract ledger lines, configured global filter, one vault walk per batch, dead rechecks removed, clippy clean in epic files. Verified: cargo fmt --check pass; cargo test --test cli 1000 passed; lib 1716 passed + 1 expected 4j kinds failure; clippy shows only pre-existing 28 deny; 7 new CLI tests (batch 2!+=x, forced flags exit 2 exact, refusals exit codes exact, exact human outputs, ledger JSON, custom filter); docs rewritten with worked example + refusal table; sandbox strike/dedupe match contract (noted). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-4i.7.1](bob-cli-4i.7.1.md) ✓ · ⧖ 2026-10-05
- **Depends on:** [bob-cli-4i.7.2](bob-cli-4i.7.2.md) ✓ · ⧖ 2026-10-05
- **Blocks:** [bob-cli-4i.7.4](bob-cli-4i.7.4.md) ◐ · ⧖ 2026-10-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4i.7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4i.7.3/README.md) | [bob-cli-4i.7.3](bob-cli-4i.7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`db1da70`](https://github.com/bobs-org/bob-cli/commit/db1da70db505d18ff21cd042de583e358ee4e09c) | feat(capture): task-complete strike/move ledger output with struck\_in and dropped | [bob-cli-4i.7.3](bob-cli-4i.7.3.md) | 2026-10-05 18:47:34 EDT |
