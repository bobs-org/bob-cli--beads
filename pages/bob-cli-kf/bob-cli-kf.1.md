# Bead: bob-cli-kf.1 — Gcal hostile title and badge URL escaping

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.1` · **Size:** small
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 13:54:00 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

gcal-escaping: collapse newlines/control whitespace in calendar titles and percent-encode whitespace in badge URLs so a synced event can no longer forge daily-note Markdown; extend the hostile-title e2e test with multi-line cases.

## Notes

[2026-11-11T18:54:00Z · bob-cli-kf.1] Collapsed control/Unicode whitespace in gcal escape_title and percent-encoded ASCII whitespace/control bytes in escape_badge_url so synced events cannot forge daily-note Markdown. Maps locations collapse before query encoding. Verified cargo test --lib native::gcal (252), cargo test --test gcal_sync hostile_titles_stay_data (multiline title plus newline/tab join URLs stay one Event Task line ending in the block id; no extra headings), just lint, and just fmt.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.1/README.md) | [bob-cli-kf.1](bob-cli-kf.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2c104b9`](https://github.com/bobs-org/bob-cli/commit/2c104b9e1e3a2553294e8cc7a5cd7d1c0e823fda) | fix(gcal): collapse hostile titles and encode badge URL whitespace | [bob-cli-kf.1](bob-cli-kf.1.md) | 2026-11-11 13:55:14 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kf.1][1] | Need notes from earlier agents | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.1/README.md

<!-- sase:referenced-by:end -->
