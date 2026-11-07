# Bead: bob-cli-ii.6 — The hollow paper-plane awaiting block mark

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.6` · **Size:** medium
**Created:** 2026-11-07 17:21:22 EST · **Closed:** 2026-11-07 17:53:37 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

mark: specify and ship the awaiting blocked-reason mark (hollow paper plane, waiting family) with its precedence, tooltip, tag fold, Tasks query CSS, conformance vectors, and contrast tests across bob-cli docs and bob-plugins.

## Notes

[2026-11-07T22:53:23Z · bob-cli-ii.6] PROPOSED FOLLOW-UP: Trim or split bob-plugins docs/bob-ledger-tools.md before more mark prose lands — the reference page sits a few words under its 6000-word reference/ budget after the awaiting mark (the first draft hit 6019 and failed npm run docs:check), so the signals phase (reply badge, no-reply pill, daily-note Gmail sync) will likely trip the cap.

[2026-11-07T22:53:37Z · bob-cli-ii.6] Shipped the awaiting blocked-reason mark. Contract: docs/blocked-marks.md gains the awaiting key (waiting family, P1 ink), the --bob-block-glyph-sent hollow plane (one 2.1-stroke path M12.75 3.25 3.25 7.25l4 1.5 1.5 4Z, no fold line so it stays hollow at 15px), precedence dep > prj > awaiting > dates with the hold owning its date (no Also scheduled pip, no digit), the "Awaiting reply from <who> · nudge …" tooltip with <who> from the first linked mail note via the metadata cache, the #awaiting_reply pill fold, the Tasks-results cascade rule, and AW1–AW7. bob-plugins: 142c model/tooltip/tag source, 142d render key, 142h/272d generalized tag folds (LP + reading), 272c mailWho lookup, styles.css paint/pip/Tasks rules (plane rules exclude prj rows explicitly because :has() outranks prj by specificity), Task Card key + reason line. Verified: npm test 5677/5677; new AW1–AW7 model, contrast (plane = P1 ink, 4.87 light / 4.70 dark), editor and reading fold, and Task Card tests; real-Obsidian e2e on athena 171/171 (10 new awaiting cases incl. hover tooltip with who, both-view folds, AW7 plane over the medium digit) with screenshots reviewed light/dark; bob-cli just docs-check and bob-plugins npm run docs:check pass; bob plugins sync --repo deployed (nav-hotkeys forced after confirming the vault copy was a strict subset of HEAD).

## Dependencies

- **Blocks:** [bob-cli-ii.7](bob-cli-ii.7.md) ◐ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.6/README.md) | [bob-cli-ii.6](bob-cli-ii.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`539b71d`](https://github.com/bobs-org/bob-cli/commit/539b71dce39ac19e958f028c833e8f4ccdb5b481) | docs(blocked-marks): specify the hollow paper-plane awaiting mark | [bob-cli-ii.6](bob-cli-ii.6.md) | 2026-11-07 17:54:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.6][1] | Check phase notes for earlier work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.6/README.md

<!-- sase:referenced-by:end -->
