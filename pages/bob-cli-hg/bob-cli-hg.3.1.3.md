# Bead: bob-cli-hg.3.1.3 — Render HTML bodies with quote folding and safe images

[Bead Pages](../README.md) / [bob-cli-hg.3.1](bob-cli-hg.3.1.md) / bob-cli-hg.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.3.md) · **Assignee:** `bob-cli-hg.3.1.3` · **Size:** medium
**Created:** 2026-11-05 13:16:21 EST · **Closed:** 2026-11-05 19:57:49 EST
**Plan:** [202611/gmail\_mail\_body.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_mail_body.md)

## Description

html-body: add the HTML5 DOM walker, quote and signature extraction, data-table versus layout-table handling, bulletin mode, and image decisions in section 5, using the established inert serializer and synthetic golden tests.

## Notes

[2026-11-06T00:57:06Z · bob-cli-hg.3.1.3] PROPOSED FOLLOW-UP: Fix the clean-base workspace test failures for overlapping clipboard catalog paths and the duplicate clipboard:count entry; both exact failures reproduce on clean HEAD 1cbe9703 and were previously recorded in bob-cli-hj.4 note #1.

[2026-11-06T00:57:49Z · bob-cli-hg.3.1.3] Implemented sanitized HTML body rendering with quote folding, safe link/image handling, CID verification, and semantic table conversion. cargo test --lib native::gmail::body:: passed (32 tests); formatting and Clippy passed. just check found two unrelated clipboard catalog tests that reproduce on clean base 1cbe9703; recorded as PROPOSED FOLLOW-UP. epic-symbols reports no leftovers.

## Dependencies

- **Depends on:** [bob-cli-hg.3.1.2](bob-cli-hg.3.1.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.3.1.4](bob-cli-hg.3.1.4.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.3.1.3/README.md) | [bob-cli-hg.3.1.3](bob-cli-hg.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`540f3e6`](https://github.com/bobs-org/bob-cli/commit/540f3e6fda16bb88bf6c58c8f7ee551ed4916230) | feat(gmail): render HTML message bodies | [bob-cli-hg.3.1.3](bob-cli-hg.3.1.3.md) | 2026-11-05 19:59:05 EST |
