# Bead: bob-cli-j9.1 — bob proves tips and stamps alias ids

[Bead Pages](../README.md) / [bob-cli-j9](README.md) / bob-cli-j9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3y.linker.w0.md) · **Assignee:** `bob-cli-j9.1` · **Size:** medium
**Created:** 2026-11-09 12:18:38 EST · **Closed:** 2026-11-09 13:10:36 EST
**Plan:** [202611/capture\_alias\_typing\_tips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_alias_typing_tips.md)

## Description

bob-alias-tips: stamp an AliasId on every forward sigil alias, add the sigil_alias_tip reverse check that runs the whole rewrite pipeline, emit tip and alias JSON from capture-rewrite, and pin it with round-trip, negative, and CLI tests plus docs.

## Notes

[2026-11-09T18:10:23Z · bob-cli-j9.1] PROPOSED FOLLOW-UP: add the alias and sigil_alias_tip fields to the capture-rewrite row in docs/reference/json-outputs.md — skipped here because that page is already over the 6000-word reference cap (bob-cli-h9); do it once the page is under budget.

[2026-11-09T18:10:36Z · bob-cli-j9.1] bob capture-rewrite now stamps every forward sigil alias with an AliasId and emits alias (on expand_sigil_alias) and sigil_alias_tip (object or explicit null; absent without --cursor or when changed) in JSON, plus one dim tip line in human output. New src/native/capture_language/alias_tip.rs runs the whole rewrite_draft pipeline per candidate key; tipped vs untipped is an exhaustive match. Verified: just test (6029 lib + 3416 cli pass), just lint (clippy gate clean, no new warnings), just docs-gen, just docs-build (strict); just docs-check fails only on 5 reference pages over the 6000-word budget that this change does not touch; the checkout build answers the documented JSON for the draft "Buy milk" plus a trailing at-sign. Two plan negatives do not hold because the forward rewrite proves them true, so they are pinned as positives: the draft "cash+goog-exit +" tips parent_task (a spaced comma still aliases plus), and the drafts "=#" and "[[folder#" tip hash_menu with keys limited to backslash (slash stays literal there; where is omitted). Mac phases should expect keys to be a subset of the candidates and where to be optional.

## Dependencies

- **Blocks:** [bob-cli-j9.3](bob-cli-j9.3.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j9.1/README.md) | [bob-cli-j9.1](bob-cli-j9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4b59ae8`](https://github.com/bobs-org/bob-cli/commit/4b59ae8170499ebc6328bc66f437af56802cfab5) | feat(capture): prove sigil alias typing tips in capture-rewrite | [bob-cli-j9.1](bob-cli-j9.1.md) | 2026-11-09 13:11:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j9.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j9.1/README.md

<!-- sase:referenced-by:end -->
