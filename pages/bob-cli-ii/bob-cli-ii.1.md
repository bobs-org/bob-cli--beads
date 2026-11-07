# Bead: bob-cli-ii.1 — Sync config and the routing-label resolver

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.1` · **Size:** medium
**Created:** 2026-11-07 17:21:21 EST · **Closed:** 2026-11-07 17:59:22 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

routing: add the gmail.sync config keys with pull fallbacks, a pure resolver that turns a thread's prefixed Gmail labels into one area or project note or a typed route problem, and doctor rows that audit every routing label.

## Notes

[2026-11-07T22:59:05Z · bob-cli-ii.1] Handoff for sync: src/native/gmail/route.rs exposes RouteContext::load(bob_dir), labels_by_id(Vec<GmailLabel>), and route(labels_by_id, thread_label_ids, enrollment_label, prefixes, &ctx) -> RouteVerdict::{Route(ResolvedParent), Unrouted, Problem(RouteProblem{kind,label,message,hint})}; kind.as_str() gives the JSON token. route() and labels_by_id() carry #[cfg_attr(not(test), allow(dead_code))] — drop those attributes once sync calls them. GmailLabel gained an optional `type` (is_user()). GmailConfig::sync_label()/sync_inbox()/route_prefixes()/reply_wait_days() resolve the pull fallbacks; pull_label()/pull_inbox() are unchanged. FakeGog::set_labels(json) overrides the fake labels list.

[2026-11-07T22:59:22Z · bob-cli-ii.1] Verified: gmail.sync config (label/inbox/route_prefixes/reply_wait_days) with pull fallbacks and key-named setup errors (unit tests in config/gmail.rs and gmail/config.rs); pure resolver src/native/gmail/route.rs with RouteContext + resolve_parent_in, vectors R1-R14 plus near-miss, ambiguous_alias, closed-project chain, and cycle tests; doctor config row extended and warn-only routes row (ok count, per-label 'label → kind · hint' lines, no-prefix skip, token-fail skip, label-list warn) tested in tests/gmail_shell.rs with fake gog labels. docs/gmail.md Configuration+Doctor and docs/reference/configuration.md updated. just lint (no new warnings), just test (9271 passed, 0 failed), just docs-check all green.

## Dependencies

- **Blocks:** [bob-cli-ii.3](bob-cli-ii.3.md) ◐ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.1/README.md) | [bob-cli-ii.1](bob-cli-ii.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6b17476`](https://github.com/bobs-org/bob-cli/commit/6b1747638b0d346189c17f934665ecfffcd88a92) | feat(gmail): add sync routing config, label resolver, and doctor routes row | [bob-cli-ii.1](bob-cli-ii.1.md) | 2026-11-07 18:00:13 EST |
