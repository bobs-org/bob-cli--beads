# Bead: bob-cli-kq.2 — Gcal remote-text trust boundary

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.2` · **Size:** medium
**Created:** 2026-11-12 05:24:40 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

gcal-title-hardening: extend gcal escape_title to neutralize mid-line tags, wikilinks, and Markdown links in organizer-authored event titles; fix the gog 429 substring misclassification; optionally gate #on/#off clock tags on organizer_is_self per the memory decision.

## Notes

[2026-11-12T10:46:43Z · bob-cli-kq.2] Verified: escape_title now neutralizing mid-line #tags, [[wikilinks]], and Markdown ]( links after clock tokens are stripped; classify_gog_failure matches 429 only as an HTTP status token so team-429@ identifiers are not retried; journal title hashes follow the escaped span so untouched Google updates rewrite once. gate_organizer_clock_tags=no so no clock-tag or memory edits. just check staged for host completion and close.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.2.md) | [bob-cli-kq.2](bob-cli-kq.2.md) | 0 |
