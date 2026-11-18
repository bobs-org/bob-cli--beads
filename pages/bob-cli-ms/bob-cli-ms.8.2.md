# Bead: bob-cli-ms.8.2 — bob writes records without an H1 and tidy removes redundant ones

[Bead Pages](../README.md) / [bob-cli-ms.8](bob-cli-ms.8.md) / bob-cli-ms.8.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.land.md) · **Assignee:** `bob-cli-ms.8.2` · **Size:** medium
**Created:** 2026-11-17 22:26:14 EST · **Closed:** 2026-11-18 08:48:59 EST
**Plan:** [202611/record\_card\_title\_and\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_title_and_proof.md)

## Description

h1-retire: bob records new, update, and capture write record notes with no H1, Notes insertion handles H1-less bodies, bob records tidy also removes an H1 that only repeats the frontmatter title, docs and tests follow, then just install and the live-vault cleanup per the first_cleanup decision.

## Notes

[2026-11-18T13:48:45Z · bob-cli-ms.8.2] h1-retire landed in workspace: render writes H1-less notes, update inserts canonical Notes, tidy removes redundant H1 (h1_removed/h1_kept + kept_h1 reasons). Live-vault cleanup done: bob records tidy committed 70dc35cb6 on ~/bob (192 scanned, 192 H1 removed, 0 empty Notes, 0 kept); re-run is a clean no-op. Spot-checked sase_blog_zettel/bead_lifecycle.md (now frontmatter-only) and eat/1950s_originals.md (Source block intact, heading null). Sheet-title deploy confirmed via bob-record-sheet-title in ledger-tools main.js. Mac Capture: RecordNotePreviewView renders body lines generically, no H1 assumption — no Swift change needed.

[2026-11-18T13:48:59Z · bob-cli-ms.8.2] h1-retire done and verified: render/update/capture write H1-less notes; tidy strips redundant H1s with counts and kept reasons. Gates green: fmt, clippy gate, docs-check, full lib (7356), full cli (3787), all other test targets, doctests. just install done; live tidy commit 70dc35cb6 (192/192 H1 removed, 0 kept), re-run clean, spot-checks pass.

## Dependencies

- **Depends on:** [bob-cli-ms.8.1](bob-cli-ms.8.1.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-ms.8.3](bob-cli-ms.8.3.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ms.8.2/README.md) | [bob-cli-ms.8.2](bob-cli-ms.8.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2f80442`](https://github.com/bobs-org/bob-cli/commit/2f80442bb2c3141b69131c6db7786516fa165ca0) | feat(records): write H1-less record notes and tidy redundant H1s | [bob-cli-ms.8.2](bob-cli-ms.8.2.md) | 2026-11-18 08:51:15 EST |
