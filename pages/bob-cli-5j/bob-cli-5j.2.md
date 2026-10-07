# Bead: bob-cli-5j.2 — Keep return-link glyphs out of synced highlights

[Bead Pages](../README.md) / [bob-cli-5j](README.md) / bob-cli-5j.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3x.linker.w0.md) · **Assignee:** `bob-cli-5j.2` · **Size:** medium
**Created:** 2026-10-07 14:27:22 EDT · **Closed:** 2026-10-07 16:06:44 EDT
**Plan:** [202610/ref\_create\_return\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_return_links.md)

## Description

export: stamp a `return_links: true` marker key on PDFs that actually carry return links, register it as a standard synced field, and strip tag glyphs and pill text from highlight text when `bob ref sync` renders the note region for those PDFs.

## Notes

[2026-10-07T20:06:32Z · bob-cli-5j.2] PROPOSED FOLLOW-UP: capture::r#ref::capture_url_with_markers_or_flags_stays_a_task fails on xclip with no display (environmental); reproduces identically on clean base tree

[2026-10-07T20:06:44Z · bob-cli-5j.2] Export phase done: return_links marker key stamped only after paired renders (Bool, after captured), strip_return_link_glyphs cleans highlight text for flagged PDFs with stable block IDs. Verified: cargo fmt clean, clippy exit 0, lib 1903 passed, CLI 1160 passed incl. new marker round-trip test; single failure is pre-existing xclip/display env failure confirmed identical on base (recorded as follow-up). epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-5j.1](bob-cli-5j.1.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5j.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5j.2/README.md) | [bob-cli-5j.2](bob-cli-5j.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6fb936d`](https://github.com/bobs-org/bob-cli/commit/6fb936d71dc0a79e59f3566b1e23c60938b9d0db) | feat(highlights): keep return-link glyphs out of synced highlights | [bob-cli-5j.2](bob-cli-5j.2.md) | 2026-10-07 16:07:53 EDT |
