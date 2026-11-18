# Bead: bob-cli-n5.4 — Honor Reply-To when drafting plain Gmail replies

[Bead Pages](../README.md) / [bob-cli-n5](README.md) / bob-cli-n5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-my.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-my.land.md) · **Assignee:** `bob-cli-n5.4` · **Size:** medium
**Created:** 2026-11-17 22:21:55 EST · **Closed:** 2026-11-18 01:12:08 EST
**Plan:** [202611/backlog\_triage\_t3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t3.md)

## Description

reply-to: Resolve bob-cli-ia with fake-gog coverage while preserving self-sent and reply-all behavior.

## Notes

[2026-11-18T06:12:08Z · bob-cli-n5.4] Honored usable Reply-To recipients for plain Gmail replies, filtered the account address, and validated malformed headers before draft operations; missing, empty, and self-only Reply-To preserve From/self-sent To fallbacks, and reply-all remains on gog's path. Verified 13 gmail_draft tests, sase tool run check (succeeded, exit 0), just docs-check (all gates passed), cargo fmt --check, and git diff --check.

## Dependencies

- **Depends on:** [bob-cli-n5.3](bob-cli-n5.3.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-n5.5](bob-cli-n5.5.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n5.4/README.md) | [bob-cli-n5.4](bob-cli-n5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f1d98b7`](https://github.com/bobs-org/bob-cli/commit/f1d98b7fc1f79a42759573ca6fa748d6a473d243) | fix(gmail): honor Reply-To for plain replies | [bob-cli-n5.4](bob-cli-n5.4.md) | 2026-11-18 01:13:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-n5.4][1] | Need phase attachments and parent epic decisions for implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n5.4/README.md

<!-- sase:referenced-by:end -->
