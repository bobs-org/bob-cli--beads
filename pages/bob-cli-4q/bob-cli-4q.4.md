# Bead: bob-cli-4q.4 — Docs, rollout log, and decision-record follow-up

[Bead Pages](../README.md) / [bob-cli-4q](README.md) / bob-cli-4q.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xh.md) · **Assignee:** `bob-cli-4q.4` · **Size:** small
**Created:** 2026-10-06 14:57:18 EDT · **Closed:** 2026-10-06 15:40:27 EDT
**Plan:** [202610/inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inbox_routing.md)

## Description

docs-and-rollout: document inbox routing in bob-cli docs (projects, freshness ritual and rollout log, getting-started, nav api §9), run the full plugin suite, deploy, and file a memory bead for a decisions strand.

## Notes

[2026-10-06T19:38:20Z · bob-cli-4q.4] PROPOSED FOLLOW-UP: file a memory task bead proposing a new decisions strand (e.g. inbox-answers-route-first): on an open inbox task, Ctrl+Shift+P commits (except closes) and Ctrl+Shift+Enter prompt for a destination as the last step, act then move, never follow, and advance as answers; Ctrl+Shift+M unchanged; list the rejected alternatives from plan 202610/inbox_routing.md plus a one-line addition to glossary:area-note about inbox routing

[2026-10-06T19:40:19Z · bob-cli-4q.4] PROPOSED FOLLOW-UP: just all shows 2 pre-existing lib failures reproducing identically on the clean base tree (docs-only change cannot cause them): native::completion::kinds::tests::every_value_arg_has_a_decision and native::highlights_ref::create::tests::listen_filter_renders_card_and_encoded_play_link; a third (capture_pomodoros missing_note warning test) fails only under full-suite parallelism and passes in isolation with this change applied

[2026-10-06T19:40:27Z · bob-cli-4q.4] Docs: projects.md Inbox routing spec + Contents, freshness.md stamping table/ritual one-key list/rollout line for nav 2.10.0 + block-id-prompt 1.23.0, getting-started inbox sentence, task-dependencies.md inboxRoute v1. Verified: bob-plugins npm test 1988 pass/0 fail (incl. inbox-route suites); bob plugins list 6 synced 0 drift, dry-run sync all up to date; just fmt+lint clean (just all lib has 2 pre-existing failures also failing on clean base, recorded as follow-up). Decision-strand memory bead filed as PROPOSED FOLLOW-UP per phase-worker rule.

## Dependencies

- **Depends on:** [bob-cli-4q.2](bob-cli-4q.2.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4q.3](bob-cli-4q.3.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4q.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4q.4/README.md) | [bob-cli-4q.4](bob-cli-4q.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ade4b8a`](https://github.com/bobs-org/bob-cli/commit/ade4b8af2580bad8bba18339180987be1a5c4849) | docs(inbox-routing): add canonical spec and rollout notes | [bob-cli-4q.4](bob-cli-4q.4.md) | 2026-10-06 15:41:38 EDT |
