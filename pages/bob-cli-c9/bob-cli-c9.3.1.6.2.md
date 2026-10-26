# Bead: bob-cli-c9.3.1.6.2 — Identity-correct family matching and attach targets

[Bead Pages](../README.md) / [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) / bob-cli-c9.3.1.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) · **Assignee:** `bob-cli-c9.3.1.6.2` · **Size:** medium
**Created:** 2026-10-25 19:48:33 EDT · **Closed:** 2026-10-25 20:30:08 EDT
**Plan:** [202610/ref\_reread\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md)

## Description

family_matching: title identity on title routes, exact-only URL family candidates, deleted-root naming, refusal reading numbers, the -o guard, and newest-reading -L attach for single sources and collections.

## Notes

[2026-10-26T00:30:02Z · bob-cli-c9.3.1.6.2--1] Implemented the family-matching phase: title-aware identity, exact URL-family selection, deleted-root naming, refusal reading numbers, the -o reread guard, and newest-reading -L attach behavior for single sources and collections. Verified cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces (exit 0), cargo fmt --check, and git diff --check.

[2026-10-26T00:30:08Z · bob-cli-c9.3.1.6.2--1] Family-matching implementation recorded; clippy, cargo fmt --check, and git diff --check passed; no epic-symbol entries remain.

## Dependencies

- **Depends on:** [bob-cli-c9.3.1.6.1](bob-cli-c9.3.1.6.1.md) ✓ · ⧖ 2026-10-25
- **Blocks:** [bob-cli-c9.3.1.6.3](bob-cli-c9.3.1.6.3.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.2.md) | [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e35773e`](https://github.com/bobs-org/bob-cli/commit/e35773e533dc567a5f45a6bc12bb01b96b21e0d0) | fix(ref): preserve family identity for rereads | [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) | 2026-10-25 20:30:46 EDT |
