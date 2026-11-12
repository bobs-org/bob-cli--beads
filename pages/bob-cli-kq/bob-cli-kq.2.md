# Bead: bob-cli-kq.2 — Gcal remote-text trust boundary

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.2` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST · **Closed:** 2026-11-12 06:23:13 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

gcal-title-hardening: extend gcal escape_title to neutralize mid-line tags, wikilinks, and Markdown links in organizer-authored event titles; fix the gog 429 substring misclassification; optionally gate #on/#off clock tags on organizer_is_self per the memory decision.

## Notes

[2026-11-12T10:46:43Z · bob-cli-kq.2] Verified: escape_title now neutralizing mid-line #tags, [[wikilinks]], and Markdown ]( links after clock tokens are stripped; classify_gog_failure matches 429 only as an HTTP status token so team-429@ identifiers are not retried; journal title hashes follow the escaped span so untouched Google updates rewrite once. gate_organizer_clock_tags=no so no clock-tag or memory edits. just check staged for host completion and close.

[2026-11-12T11:23:13Z · bob-cli-kq.2--1] Closed by explicit `sase stitch create -B close` after create_commit landed 4ffa85d0 ("fix(gcal): escape organizer title tags and links"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-kq.2` if more work remains.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.2.md) | [bob-cli-kq.2](bob-cli-kq.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4ffa85d`](https://github.com/bobs-org/bob-cli/commit/4ffa85d03376aa5747dbb10070658f1a452a56a4) | fix(gcal): escape organizer title tags and links | [bob-cli-kq.2](bob-cli-kq.2.md) | 2026-11-12 06:22:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kq.2--1][1] | Need the phase scope, notes, and current status after host-completion failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.2.md

<!-- sase:referenced-by:end -->
