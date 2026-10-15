# Bead: bob-cli-7v.5 — Collection route - classify, capture, compose, stamp, install, report

[Bead Pages](../README.md) / [bob-cli-7v](README.md) / bob-cli-7v.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.5` · **Size:** medium
**Created:** 2026-10-15 12:30:28 EDT · **Closed:** 2026-10-15 13:56:29 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

## Description

route: replace the stub with the all-or-nothing pipeline (per-part classification, sequential render:false captures, metadata derivation, compose, list-valued marker, stamp, guarded install), dry-run and success reports, explicit --audio, and fake-adapter integration tests.

## Notes

[2026-10-15T17:56:29Z · bob-cli-7v.5--1] Replaced the collection stub with the all-or-nothing classify/capture/compose/stamp/install pipeline. just check passed (exit 0). Verified: list source_url marker plus id; scan writes one note and one ^ref task; find by part URL; later overlapping create refuses; failed part 2 writes nothing; classified/captured PDF parts refused; dry-run writes: none and skips compose; _2 collision walk and -o exact path; explicit --audio; 2- and 3-part success reports; -L still deferred. No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-7v.3](bob-cli-7v.3.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-7v.4](bob-cli-7v.4.md) ✓ · ⧖ 2026-10-15
- **Blocks:** [bob-cli-7v.6](bob-cli-7v.6.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7v.5.md) | [bob-cli-7v.5](bob-cli-7v.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9bdb0bd`](https://github.com/bobs-org/bob-cli/commit/9bdb0bd9eadbb0382f06f5815ebc51019e94ae9a) | feat(highlights-ref): wire the multi-url collection capture pipeline | [bob-cli-7v.5](bob-cli-7v.5.md) | 2026-10-15 13:57:29 EDT |
