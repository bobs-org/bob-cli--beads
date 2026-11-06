# Bead: bob-cli-hg.6.1.1 — Confirm Gmail identities and apply save refusal rules

[Bead Pages](../README.md) / [bob-cli-hg.6.1](bob-cli-hg.6.1.md) / bob-cli-hg.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) · **Assignee:** `bob-cli-hg.6.1.1` · **Size:** medium
**Created:** 2026-11-05 23:47:35 EST · **Closed:** 2026-11-06 00:55:57 EST
**Plan:** [202611/gmail\_save\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md)

## Description

resolve-policy: implement the shared read-only URL/ID/note resolver and never_save policy described in sections 3 and 4.1. Confirm exact account/thread identity, preserve typed failures, add read-only label-name lookup, and extend the fake gog with faithful synthetic scenarios. Do not write the vault.

## Notes

[2026-11-06T05:55:41Z · bob-cli-hg.6.1.1--1] PROPOSED FOLLOW-UP: clean-base failures are outside the Gmail resolver/policy diff: at clean HEAD cfdb68c1, cargo test -p bob-obsidian --lib reproduced the duplicate clipboard catalog/completion failures (tracked by bob-cli-hp), and --test cli reproduced three capture verdict assertion failures, catalog 73-vs-72 (tracked by bob-cli-de), and the stale root-help snapshot. The library target had 5329 passed, 2 failed, 2 ignored; CLI had 3238 passed, 5 failed. The focused Gmail test run passed before just check ran.

[2026-11-06T05:55:57Z · bob-cli-hg.6.1.1--1] Implemented read-only Gmail identity resolution and never_save policy with fake-gog scenarios; cargo test --lib native::gmail passed. just check failure was isolated to two lib and five CLI tests, all reproduced on clean HEAD cfdb68c1; clean-base evidence and existing trackers bob-cli-hp/bob-cli-de are recorded as a proposed follow-up. epic-symbols is empty.

## Dependencies

- **Blocks:** [bob-cli-hg.6.1.2](bob-cli-hg.6.1.2.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.1.md) | [bob-cli-hg.6.1.1](bob-cli-hg.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cdc4003`](https://github.com/bobs-org/bob-cli/commit/cdc40030d9ebc5fcd422a6d430ac9c6c3412542b) | feat(gmail): implement identity resolution and save policy | [bob-cli-hg.6.1.1](bob-cli-hg.6.1.1.md) | 2026-11-06 00:57:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.1--1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-hg.6.1.2][2] | check dep work for API reuse | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.2/README.md

<!-- sase:referenced-by:end -->
