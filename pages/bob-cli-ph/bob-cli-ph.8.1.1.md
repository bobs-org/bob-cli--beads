# Bead: bob-cli-ph.8.1.1 — Repair the drawer annotation build and cover the landed decoding

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.1` · **Size:** small
**Created:** 2026-11-25 20:55:59 EST · **Closed:** 2026-11-25 22:42:09 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

annotation-build-repair: fix the CaptureDrawerSummary marker decode that broke Mac master at b45b1951, compile every target, and add portable coverage for the drawer annotation decoding and verbatim destination labels already landed.

## Notes

[2026-11-26T03:42:09Z · bob-cli-ph.8.1.1--4] Verified exact-SHA macOS CI run 45746741457 on snapshot a553cde880204896c52b106a4e7f5d7126593f passed, and portable-check on the same snapshot completed successfully on Athena (monitor 8e0x2eash6nn).

## Dependencies

- **Blocks:** [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.3](bob-cli-ph.8.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md) | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@b0062be`](https://github.com/bobs-org/bob-mac-capture/commit/b0062be1749f388a849c5bf0251c7fb3f914bf94) | fix(mac-capture): decode drawer summary markers safely | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2026-11-25 21:11:04 EST |
| bob-mac-capture | [`bob-mac-capture@5073564`](https://github.com/bobs-org/bob-mac-capture/commit/5073564e3ce639eca04bd05659b1a5e6fd04a0f8) | test(mac-capture): align drawer assertions with true-case output | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2026-11-25 21:37:30 EST |
| bob-mac-capture | [`bob-mac-capture@4c36dd0`](https://github.com/bobs-org/bob-mac-capture/commit/4c36dd027dd07baa29c09fd021a4ef1f50d9b935) | test(mac-capture): update drawer presentation fixtures | [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) | 2026-11-25 22:43:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.8.1.1--1][1] | Need phase scope, prior notes, and design file before continuing after CI failure | 2 |
| read-by | [agent:bob-cli-ph.8.1.1--4][1] | Inspect epic state and children before closing verified work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.1.md

<!-- sase:referenced-by:end -->
