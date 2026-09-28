# Bead: bob-cli-2d.1 — Command skeleton, CLI contract, config, and model

[Bead Pages](../README.md) / [bob-cli-2d](README.md) / bob-cli-2d.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2t.md) · **Assignee:** `bob-cli-2d.1` · **Size:** medium
**Created:** 2026-09-28 13:31:28 EDT · **Closed:** 2026-09-28 13:51:38 EDT
**Plan:** [202609/bob\_gkeep\_inbox\_drain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_gkeep_inbox_drain.md)

## Description

skeleton: register `bob gkeep` and pin the whole CLI surface, including help, typed args, and stub handlers. Add the `gkeep:` config section, the note model with its canonical content and fingerprint, UI helpers, and the small visibility promotions later phases need.

## Notes

[2026-09-28T17:51:23Z · bob-cli-2d.1] PROPOSED FOLLOW-UP: cargo clippy --all-targets fails on pre-existing clippy::logic_bug deny error at tests/cli.rs:31818 (|| true makes a schedule-log assertion vacuous); byte-identical on clean HEAD, unrelated to gkeep skeleton — related warning-tracking bead bob-cli-v

[2026-09-28T17:51:38Z · bob-cli-2d.1] Skeleton complete and verified: bob gkeep + doctor/list/login/pull registered with pinned help, typed args, stubs (exit 1), gkeep config section + resolve/validate/token-shape/device-id, protocol model with pinned fp/REF/canonical tests, ui helpers. cargo fmt clean; full cargo test green (1065 lib + 515 cli + 6 gkeep_cli + others, 0 failures). cargo clippy has one pre-existing deny error at tests/cli.rs:31818 identical on clean HEAD (recorded as follow-up, cf. bob-cli-v); no new diagnostics.

## Dependencies

- **Blocks:** [bob-cli-2d.2](bob-cli-2d.2.md) ◐ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2d.3](bob-cli-2d.3.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2d.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2d.1/README.md) | [bob-cli-2d.1](bob-cli-2d.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`55fdb18`](https://github.com/bobs-org/bob-cli/commit/55fdb18d199f6d7d04ce20f4b8e26209f1b130f6) | feat(gkeep): add command skeleton, CLI contract, config, and model | [bob-cli-2d.1](bob-cli-2d.1.md) | 2026-09-28 13:53:12 EDT |
