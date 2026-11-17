# Bead: bob-cli-mj.1 — bob-cli: the video attachment kind

[Bead Pages](../README.md) / [bob-cli-mj](README.md) / bob-cli-mj.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.63.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.63.linker.w0.md) · **Assignee:** `bob-cli-mj.1` · **Size:** medium
**Created:** 2026-11-16 17:31:30 EST · **Closed:** 2026-11-16 18:31:22 EST
**Plan:** [202611/video\_attachments\_z\_player.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/video_attachments_z_player.md)

## Description

cli-video: add AttachmentKind::Video (mp4 mov webm mkv) copied to vid/ and embedded at 400 px on every %c route and bob attachments import; add size_bytes to attachment JSON and sizes to human output; fix the would-save padding; write the shared media catalog in docs/attachments.md; mark the commit with !.

## Notes

[2026-11-16T23:31:22Z · bob-cli-mj.1] cli-video done in 36e79ad3 (feat(capture)!): AttachmentKind::Video (mp4/mov/webm/mkv) copied to vid/ and embedded at 400px on every %c route and bob attachments import; size_bytes in capture clip and import JSON plus dimmed sizes in human output; would-save padding fixed; shared byte formatter; media catalog in docs/attachments.md. Verified: full cargo test --workspace green (7253 lib + all integration binaries), just lint/fmt/docs-check green, end-to-end %c smoke writes ![[vid/20261116_155943.mp4|400]] with size suffix.

## Dependencies

- **Blocks:** [bob-cli-mj.3](bob-cli-mj.3.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mj.4](bob-cli-mj.4.md) ◐ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mj.5](bob-cli-mj.5.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.1/README.md) | [bob-cli-mj.1](bob-cli-mj.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ff563eb`](https://github.com/bobs-org/bob-cli/commit/ff563ebd884836da71209ca601bbdc3409b10c1e) | feat(capture)!: embed clipboard videos from vid/ | [bob-cli-mj.1](bob-cli-mj.1.md) | 2026-11-16 18:33:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mj.1][1] | Confirm phase closed after final submit | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mj.1/README.md

<!-- sase:referenced-by:end -->
