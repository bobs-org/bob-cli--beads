# Bead: bob-cli-r8.1 — Poseidon chezmoi isolation test matches the Mac cargo config

[Bead Pages](../README.md) / [bob-cli-r8](README.md) / bob-cli-r8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md) · **Assignee:** `bob-cli-r8.1` · **Size:** small
**Created:** 2026-11-27 13:01:15 EST · **Closed:** 2026-11-27 13:09:52 EST
**Plan:** [202611/task\_bead\_burndown\_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md)

## Description

chezmoi-isolation: update the chezmoi poseidon_chezmoi_isolation_test to the intent of 9430387a (the Mac renders a debug-info-only cargo config but still ignores the poseidon files), then close bob-cli-id.

## Notes

[2026-11-27T18:09:52Z · bob-cli-r8.1] Completed the chezmoi isolation test update and closed bob-cli-id. Verified: bashunit tests/bash/poseidon_chezmoi_isolation_test.sh (4/4, 17 assertions); just test-bash (635/635, 3,141 assertions); git diff --check passed. sase bead epic-symbols bob-cli-r8.1 reported no --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-r8.2](bob-cli-r8.2.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.1/README.md) | [bob-cli-r8.1](bob-cli-r8.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@662569a`](https://github.com/bbugyi200/dotfiles/commit/662569a34eb9209baa03e4cc50d32356ee2c7a08) | test(chezmoi): align poseidon isolation assertions | [bob-cli-r8.1](bob-cli-r8.1.md) | 2026-11-27 13:11:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r8.1][1] | Confirm this phase's final status and close note | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.1/README.md

<!-- sase:referenced-by:end -->
