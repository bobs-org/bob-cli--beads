# Bead: bob-cli-hg.12.1.6 — Compose guide and consumer contract acceptance

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.6` · **Size:** small
**Created:** 2026-11-06 07:12:30 EST · **Closed:** 2026-11-06 15:52:33 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

compose-docs: finish the guide and Bob Mail JSON fixtures, audit acceptance coverage, and supply land evidence from section 4.6; do not close ancestor beads.

## Notes

[2026-11-06T20:27:55Z · bob-cli-hg.12.1.6] --list

[2026-11-06T20:52:10Z · bob-cli-hg.12.1.6] PROPOSED FOLLOW-UP: capture::complete_themes::theme_recent_shell_description_and_quoted_replacement fails in full-suite runs (asserts "recent · Oct 23 · 1 day" at complete_themes.rs:274) but passes alone on both the clean base and this branch; looks like a date-sensitive flake in the full just check run, unrelated to gmail compose-docs which touches no capture code

[2026-11-06T20:52:33Z · bob-cli-hg.12.1.6] compose-docs done: docs/gmail.md gains send command, Writing and sending section (dry-run, digest confirmation, recovery outcomes, in-place promotion, [!mail-sent]), fixed stale sending-later-work notes; new docs/guides/send-email-from-obsidian.md indexed in guides/index.md, mkdocs nav, by-component.md (via docs-gen) and linked from connect-google-mail.md; tests/fixtures/gmail_compose/ holds 6 synthetic schema-1 fixtures pinned by tests/gmail_compose_contract.rs (3 tests). Verified: contract 3/3, gmail_send 3/3, gmail_draft 5/5, docs-gen + docs-check pass, fmt+clippy clean, full just check green except unrelated capture theme_recent_shell flake (passes alone on base and branch; recorded as PROPOSED FOLLOW-UP). Acceptance audit: threading flags, refusals, digest invalidation, non-TTY confirm, 3 recovery outcomes, promotion, Reply removal, no direct-send, no-body-in-journal each map to named tests in gmail_draft/gmail_send/render+send unit tests.

## Dependencies

- **Depends on:** [bob-cli-hg.12.1.5](bob-cli-hg.12.1.5.md) ✓ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.6/README.md) | [bob-cli-hg.12.1.6](bob-cli-hg.12.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae624e2`](https://github.com/bobs-org/bob-cli/commit/ae624e2791aafc17d099cdf84244d7238787c625) | docs(gmail): document compose send flow and pin contract fixtures | [bob-cli-hg.12.1.6](bob-cli-hg.12.1.6.md) | 2026-11-06 15:54:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.12.1.6][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.6/README.md

<!-- sase:referenced-by:end -->
