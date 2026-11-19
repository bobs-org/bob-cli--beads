# Bead: bob-cli-nh.2 — bob periods update guarded envelope and day subjects in show

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.2` · **Size:** medium
**Created:** 2026-11-19 09:35:21 EST · **Closed:** 2026-11-19 15:08:04 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

update: add `bob periods update <SUBJECT> -i FILE|-`, the guarded JSON envelope the card editor writes through. It has intention, reflection, and summary ops, a field fingerprint as `expect`, dry run, inverse_ops for Undo, the vault lock, and atomic writes. Teach `bob periods show` day subjects, update help and docs, and run `just docs-gen`.

## Notes

[2026-11-19T19:10:39Z · bob-cli-nh.2--1] PROPOSED FOLLOW-UP: Land the local Justfile re-key of the three implemented intention API symbols to the open parent epic before closing this phase; the close guard still sees their stale bob-cli-nh.2 keys on origin/master.

[2026-11-19T20:07:16Z · bob-cli-nh.2] PROPOSED FOLLOW-UP: `just docs-check` still reports docs/reference/mac-capture/capture-previews.md (6096/6000 words) and keyboard.md (6027/6000); those mounted references are unchanged in this phase and the recurring over-budget issue was previously tracked by bob-cli-jz, which closed after an earlier trim.

[2026-11-19T20:08:04Z · bob-cli-nh.2] Verified existing implementation landed in a0b91a8d; `just docs-gen` passed (docs_reference 1/1), and `cargo test --test cli periods_update` passed (8/8). `sase bead epic-symbols bob-cli-nh.2` reports no remaining phase symbols. `just docs-check` is blocked only by unchanged mounted Mac Capture reference word budgets (6096 and 6027), recorded in note #2 and previously tracked by bob-cli-jz.

## Dependencies

- **Depends on:** [bob-cli-nh.1](bob-cli-nh.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.7](bob-cli-nh.7.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.2/README.md) | [bob-cli-nh.2](bob-cli-nh.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a0b91a8`](https://github.com/bobs-org/bob-cli/commit/a0b91a8dfcc27a24d35a6c13989559d7fc594450) | feat(periods): add guarded intention updates | [bob-cli-nh.2](bob-cli-nh.2.md) | 2026-11-19 14:12:26 EST |
| bob-cli | [`d84956c`](https://github.com/bobs-org/bob-cli/commit/d84956cc99792d370eaebe98466c677671a3bf1f) | docs(glossary): regenerate reference glossary | [bob-cli-nh.2](bob-cli-nh.2.md) | 2026-11-19 15:09:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.2--1][1] | Confirm close guard status and the recorded symbol follow-up | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.2.md

<!-- sase:referenced-by:end -->
