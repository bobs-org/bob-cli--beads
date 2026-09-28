# Bead: bob-cli-29.6 — Finish the =x Pomodoro close contract in bob-cli and Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-29](README.md) / bob-cli-29.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-29.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-29.land.md) · **Assignee:** `bob-cli-29.6.land`
**Created:** 2026-09-28 09:06:29 EDT · **Closed:** 2026-09-28 10:18:51 EDT
**Plan:** [202609/pomodoro\_close\_closeout.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_close_closeout.md)

## Description

Close the gaps the bob-cli-29 land audit found. In bob-cli, `bob capture =x` and its link forms honor the plan's JSON, human, and diagnostic contract for any `-b` path, with the required tests. In Bob Mac Capture, the close preview, footer, palette, and notifications match the plan's mac spec, use fixtures generated from the fixed bob, and pass macOS CI.

## Notes

[2026-09-28T14:18:51Z · bob-cli-29.6.land] Verified both closed phases and all notes: ec31329 fixes relative -b path staging, JSON raw/carried/placement/null/text, diagnostics and human output, clippy warnings introduced by this epic, docs, and byte-exact/protocol tests; aa4e156 and 67e1498 implement Mac close decode, card, model, notifications, real-bob fixtures and tests. cargo fmt --check and cargo test --quiet pass (967+498+27+31+1); macOS CI run 36433589389 passed on 67e1498. Clippy has only the preexisting bob-cli-28 || true error and older warnings. No PROPOSED FOLLOW-UP entries in either child, so no task was created or declined. Git history shows no non-epic changes after 6b22585 in bob-cli or after 4351e1c in Mac master needing integration; 395545c preceded the Mac feature and does not conflict. Epic symbols: none. Both linked plans validate. just check and just symvision recipes are absent; global plan-link validator flags older 202607 prompt archive entries unrelated to this epic.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-29.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-29.6.land/README.md) | [bob-cli-29.6](bob-cli-29.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@d5f9dd0`](https://github.com/bobs-org/bob-cli--plans/commit/d5f9dd094181919e279f40589d147d1c36163b52) | docs(plan): mark Pomodoro close epics done | [bob-cli-29.6](bob-cli-29.6.md) | 2026-09-28 10:20:42 EDT |
