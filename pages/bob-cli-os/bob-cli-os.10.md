# Bead: bob-cli-os.10 — Podcast surfaces across repos and the legacy refs

[Bead Pages](../README.md) / [bob-cli-os](README.md) / bob-cli-os.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5r.linker.w0.md) · **Assignee:** `bob-cli-os.10` · **Size:** small
**Created:** 2026-11-21 14:59:42 EST · **Closed:** 2026-11-22 03:39:16 EST
**Plan:** [202611/spotify\_episode\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/spotify_episode_refs.md)

## Description

rollout: give podcasts refs their own kind in Bob Mac Capture, the reading board, and refs.base, upgrade the two legacy refs per decision, and author the optional decision record.

## Notes

[2026-11-22T08:38:49Z · bob-cli-os.10] PROPOSED FOLLOW-UP: Podcast -f overwrite/reread reports omit the dossier lines — `bob ref create -f=overwrite <episode>` (real and -d) printed only the generic overwrite block (title/earlier/task/sync) with no capture:, duration:, pages:, feed:, or transcript: lines, though both legacy upgrades did attach publisher transcripts (59 and 37 pp). The plan promises honest reports naming everything attached; extend the overwrite_podcast report to match the fresh-create block.

[2026-11-22T08:38:56Z · bob-cli-os.10] PROPOSED FOLLOW-UP: bob plugins sync inclusion proof misses on a dirty checkout — from a dirty bob-plugins tree sync refused bob-ledger-tools ("no single commit reachable from HEAD holds the stamped bundle byte for byte") although landed ancestor f703f1c held all three deployed assets byte for byte; after git stash the same HEAD found the proof. The proof should not depend on worktree cleanliness (related to the clean-stamp note on bob-cli-on.10.1.2).

[2026-11-22T08:39:03Z · bob-cli-os.10] PROPOSED FOLLOW-UP: Mac Capture docs-check fails on 3 bob-cli tools/docs test_contracts tests (55 vs 54 registry entries; task-split.md vs task-requirements.md; README digest) — reproduces identically on clean bob-cli master, already tracked in epic bob-cli-on notes; no new bead needed unless that epic drops it.

[2026-11-22T08:39:16Z · bob-cli-os.10] Rollout done. Mac Capture: RefKind.podcast (podcasts → "Podcast", SF Symbol mic, cyan tint since purple is chat, kind words podcast/episode, author caption, page-1 dossier thumbnail) + RefsModel/RefsRanking tests + refs-inspector doc; athena portable-check green (2678 tests), mac bundle.sh + typecheck-tests green, exact-SHA macOS CI run 45001865708 green on snapshot 4c487b0c. bob-plugins: READING_BOARD_KIND_MAP podcasts 🎙️ Podcast + test + fixture KINDS; build/build:check/validate ok, reading-board tests green (npm test: only 2 load-sensitive perf tests failed at load avg 146, both pass in isolation); deployed via landed-recipe clean sync (inclusion proof f703f1c) then dirty sync, vault main.js carries the entry. Vault refs.base: /podcasts → "🎙️ Podcast" before the 🔖 Ref fallback (vault commit b2b3ce594). legacy_refs=yes: freshly built bob renamed 4ugvfwty2i8hgagsvt7pjc → software_factories_and_code_reviews_with_harjot_gill and 5ygcxo9nxh38ns7ghtbddm → software_engineering_after_code_becomes_cheap_with_satya_nadella, then -f=overwrite with canonical URLs: both PDFs are episode dossiers (59/37 pp, chapter ?t= links, publisher transcripts), tasks still [x] with ^ref block ids kept, wikilinks rewritten, zettel block link resolves, refs stay under blogs/, si-suffixed URL resolves. decision_record=no: no memory written.

## Dependencies

- **Depends on:** [bob-cli-os.9](bob-cli-os.9.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-os.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-os.10/README.md) | [bob-cli-os.10](bob-cli-os.10.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@310c946`](https://github.com/bobs-org/bob-mac-capture/commit/310c946b0e2f0880a623dc7453e8a4c455ff883e) | feat(refs): give podcasts refs their own Podcast kind | [bob-cli-os.10](bob-cli-os.10.md) | 2026-11-22 03:40:07 EST |
| bob-plugins | [`bob-plugins@e7427ad`](https://github.com/bobs-org/bob-plugins/commit/e7427ad9f61306da00cd605b70e12060a1045162) | feat(ledger-tools): label podcasts refs on the Reading Board | [bob-cli-os.10](bob-cli-os.10.md) | 2026-11-22 03:40:46 EST |
