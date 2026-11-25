# Bead: bob-cli-pw.5.1.3 — Replace meeting notes while preserving recap ownership and task identity

[Bead Pages](../README.md) / [bob-cli-pw.5.1](bob-cli-pw.5.1.md) / bob-cli-pw.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pw.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.5.md) · **Assignee:** `bob-cli-pw.5.1.3` · **Size:** medium
**Created:** 2026-11-24 15:14:21 EST · **Closed:** 2026-11-24 20:11:04 EST
**Plan:** [202611/ref\_meet\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_meet_cli.md)

## Description

replacement: wire meeting overwrite into the existing recapture/overwrite transaction. Preserve reference and reading-task identity, LINKS bytes, and user-edited recap; replace only owned recap inside the transaction, keep recap out of ref_history, and preserve existing coordination, rollback, and recovery.

## Notes

[2026-11-25T01:10:47Z · bob-cli-pw.5.1.3] PROPOSED FOLLOW-UP: just lint/check fails on HEAD with clippy::useless_format in src/native/highlights_ref/intake.rs:1233 (already-filed re-root message) — reproduces on clean bf309445 without this phase

[2026-11-25T01:11:04Z · bob-cli-pw.5.1.3] Wired meeting overwrite into the recapture/overwrite transaction: owned recap reseeds, edited/malformed recap is preserved with a warning, recap stays off ref_history when meeting_recap is set, identity/LINKS/default status stay, explicit status updates, source store history grows, Google/manual dedupe refuse without -O, -O with no occurrence files as new, renamed notes keep the live path, producer subjects are bob ref meet: overwrite meetings/{stem} while create stays bob ref create. Recap apply is inside execute (AfterNote rollback restores the preimage). No leftover --epic-symbol entries. Focused tests: meetings recap helpers, overwrite execute recap/producer/failpoint/preimage, create::meet_route (13). just lint still fails on HEAD clippy::useless_format in intake.rs:1233 (recorded as PROPOSED FOLLOW-UP).

## Dependencies

- **Depends on:** [bob-cli-pw.5.1.2](bob-cli-pw.5.1.2.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pw.5.1.4](bob-cli-pw.5.1.4.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.5.1.3/README.md) | [bob-cli-pw.5.1.3](bob-cli-pw.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c5fa6da`](https://github.com/bobs-org/bob-cli/commit/c5fa6da65e33d16ac6591ec2ec32c0280a47bbdf) | feat(meet): overwrite filed notes while preserving recap and identity | [bob-cli-pw.5.1.3](bob-cli-pw.5.1.3.md) | 2026-11-24 20:14:27 EST |
