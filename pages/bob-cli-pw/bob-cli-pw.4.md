# Bead: bob-cli-pw.4 — Marker-carried meeting identity births the LINKS relation and recap

[Bead Pages](../README.md) / [bob-cli-pw](README.md) / bob-cli-pw.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.65.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.65.linker.w0.md) · **Assignee:** `bob-cli-pw.4` · **Size:** medium
**Created:** 2026-11-24 10:38:46 EST · **Closed:** 2026-11-24 14:04:53 EST
**Plan:** [202611/meeting\_notes\_event\_refs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/meeting_notes_event_refs.md)

## Description

meeting-birth: intake and sync births for a meetings PDF whose marker carries `event` give the reading task a LINKS child and seed the note's recap from the birth store, byte-identical whether ingested inline or later by `bob ref scan`.

## Notes

[2026-11-24T19:04:31Z · bob-cli-pw.4] PROPOSED FOLLOW-UP: just lint/clippy currently fails on clean tree in src/native/props/contract/read.rs and src/native/props/cli.rs (collapsible_if, for_kv, etc.); meeting-birth passes its own tests and fmt, but the full just check gate stays red until those pre-existing lints are fixed

[2026-11-24T19:04:53Z · bob-cli-pw.4] Meeting birth lands: meetings PDFs with marker event birth LINKS (notes from, validated, no effect) + full owned recap from birth store dossier, byte-identical inline via ref sync and queued via scan -i. Verified: 6 unit tests (meeting_birth glue, birth helpers, config) + 5 CLI tests (full recap, missing store/event, inline-vs-drain identical, second-sync/adopt preservation, no dangling LINKS). fmt clean; clippy pre-existing props failures recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-pw.1](bob-cli-pw.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pw.5](bob-cli-pw.5.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.4/README.md) | [bob-cli-pw.4](bob-cli-pw.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`923df1a`](https://github.com/bobs-org/bob-cli/commit/923df1a63e771bcaa13488b3e0bc64152b97cac4) | feat(meetings): marker-carried meeting identity births LINKS relation and recap | [bob-cli-pw.4](bob-cli-pw.4.md) | 2026-11-24 14:06:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pw.4][1] | Need full JSON with notes | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.4/README.md

<!-- sase:referenced-by:end -->
