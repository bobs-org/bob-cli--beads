# Bead: bob-cli-ii.2 — Turn classification and mail-note turn fields

[Bead Pages](../README.md) / [bob-cli-ii](README.md) / bob-cli-ii.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19q.md) · **Assignee:** `bob-cli-ii.2` · **Size:** medium
**Created:** 2026-11-07 17:21:21 EST · **Closed:** 2026-11-07 18:18:13 EST
**Plan:** [202611/gmail\_sync\_reply\_watch.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_reply_watch.md)

## Description

turns: classify each Gmail message as your move, their move, automated, bounce, or ignored, fold a thread into whose turn it is, write turn and turn_since into mail notes, and upgrade an untouched mail.base with a Waiting for reply view.

## Notes

[2026-11-07T23:16:13Z · bob-cli-ii.2] gog header coverage (step 2): gog v0.44.0 (installed on athena) through upstream HEAD v0.48.0+ has NO `--format` flag on `gmail thread get` ("unknown flag --format"); it always calls Threads.Get(...).Format("full"), so every message carries all payload headers (From/To/Cc/Bcc/Auto-Submitted/X-Autoreply/X-Autorespond/Precedence/Content-Type) plus bodies. Bob's Gog::thread_metadata passed `--format metadata`, so bob gmail search, peek, list -r, and send recovery all failed against real gog while the fake accepted the flag. Fixed: thread_metadata now runs plain `gmail thread get <id>` (no --format, no --full); fake gog now rejects `--format` on thread get and serves the metadata scenario when `--full` is absent. The watch phase should fetch watched threads through thread_metadata.

[2026-11-07T23:16:19Z · bob-cli-ii.2] Also fixed a pre-existing mail-note refresh bug: note::parse heading_range/summary_range included the line ending, so every refresh that rewrote title/summary ate one newline; two refreshes fused "# Title" with the Open-in-Gmail line and "· summary" with "## Notes". Ranges now end at content_end (as card header ranges already did); merge test repeated_refreshes_keep_the_blank_lines_around_title_and_summary pins it. Needed because a changed turn alone now triggers a refresh. Vault mail notes checked: none damaged yet.

[2026-11-07T23:16:23Z · bob-cli-ii.2] PROPOSED FOLLOW-UP: gog metadata-only thread read — upstream gog `gmail thread get` has no --format metadata/--headers, so Bob's thread_metadata (search, peek, list -r, send recovery, and the sync watch loop every 15 min) downloads full bodies; propose to openclaw/gogcli adding `--format metadata --headers H1,H2` to `gmail thread get` (needed headers: From, To, Cc, Bcc, Subject, Date, Message-ID, Auto-Submitted, X-Autoreply, X-Autorespond, Precedence, Content-Type), then switch thread_metadata to it behind a version check.

[2026-11-07T23:16:27Z · bob-cli-ii.2] PROPOSED FOLLOW-UP: `gog gmail search --ids-only` needs gog >= v0.48.0 (added in gogcli 6ad392fc, #1257) but Bob's gog gate is >= v0.44.0 and athena runs v0.44.0 ("unknown flag --ids-only") — Gog::search_page (resolve.rs RFC message-ID lookup today, and the planned bob gmail sync paged discovery) fails on older gog; raise the minimum gog to v0.48.0 (or gate the ids-only path) before the sync phase ships, and verify the Mac's gog version.

[2026-11-07T23:18:13Z · bob-cli-ii.2] Verified: new pure src/native/gmail/turn.rs (classify + fold, unit vectors T1-T12 plus marker, ordering, and unproven-direction cases); mail notes write turn/turn_since after messages on save/refresh/link/send promotion (changed turn = refresh, unknown removes both); bob gmail list -f json exposes turn/turn_since (null when absent); mail.base gains the Waiting for reply view (turn == theirs, turn_since ASC, title/who/turn_since/file.backlinks), MAIL_BASE_V1 kept, untouched V1 upgraded only in a write that creates/refreshes a note and is committed, customized base left alone. gog check: thread get has no --format (fixed thread_metadata; fake gog now rejects it); fake-gog contract test tests/gmail_turns.rs drives every classifier header through gog JSON. Also fixed refresh newline loss in note::parse ranges. Docs: gmail.md Save/List/Security, vault-format.md, json-outputs.md. cargo fmt --check, just lint (exit 0, no new warnings), cargo test --workspace (9255 passed, 0 failed), just docs-check all green. Follow-ups recorded as notes (gog metadata thread read; --ids-only needs gog >= 0.48.0).

## Dependencies

- **Blocks:** [bob-cli-ii.4](bob-cli-ii.4.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.7](bob-cli-ii.7.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.2/README.md) | [bob-cli-ii.2](bob-cli-ii.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4734146`](https://github.com/bobs-org/bob-cli/commit/47341462a6d15a6c6074c1eba45d00eeaee2f7b2) | feat(gmail): record whose turn a thread is in on mail notes | [bob-cli-ii.2](bob-cli-ii.2.md) | 2026-11-07 18:19:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.2][1] | check notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.2/README.md

<!-- sase:referenced-by:end -->
