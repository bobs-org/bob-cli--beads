# Bead: bob-cli-c9.3.1.1 — Parse recapture modes and preserve existing force behavior

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.md) · **Assignee:** `bob-cli-c9.3.1.1` · **Size:** medium
**Created:** 2026-10-25 15:22:58 EDT · **Closed:** 2026-10-25 16:20:22 EDT
**Plan:** [202610/ref\_create\_reread.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_reread.md)

## Description

force_parser: implement the force-mode parser, option plumbing, completion, and parser tests; retain filed-reference refusals until the reread writers land.

## Notes

[2026-10-25T20:20:22Z · bob-cli-c9.3.1.1] force_parser done. New src/native/highlights_ref/force.rs: ForceMode::{Reread,Overwrite}, spec'd clap arg (num_args 0..=1, require_equals, default_missing reread, possible values, ignore_case), after-only adoption via clap indices with bareness read from raw argv (bare and --force= are index-identical in clap 4.6.7: flag slot + one value slot), stray-mode guard (exact or edit distance <=2, escapes ./x [[x] existing-path URL), missing-target re-parse for byte-identical usage error. Option<ForceMode> through CreateOptions/ClipOptions/collection; low-level bool perms via is_some(); unrelated commands' force flags untouched. Overwrite triage: filed refs exit 2 '-f overwrite is not available yet for filed references'; fresh sources exit 1 'nothing to overwrite: <source> is not a reference yet' + hint; queued-only/exact-output/audio keep old perms; -L attach preserved. Help: -f row + Recapture section (honest interim limits); completion automatic via clap choices (group mode, !prefix 8). Verified: 14 force unit tests (full matrix), 13 new CLI tests (guard/adoption/missing-target/repeat/invalid/fresh/filed/queued/clip-alias/glued/collection + no-fetch no-adapter no-write proofs), full highlights lib 751 + CLI 399 + completion/help/docs 146 + ref_library/aliases 185 all green; cargo fmt clean; clippy gate 0 errors; just docs-gen + docs-check pass (ref.md golden unchanged: member help not captured). Deviation from matrix: '-foverwrite URL' is NOT clap UnknownArgument — '-o' owns short o so it parses as '-f -o verwrite' and fails on the output-path extension (verified byte-identical to spaced form); help documents this and a test locks it.

## Dependencies

- **Blocks:** [bob-cli-c9.3.1.2](bob-cli-c9.3.1.2.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.1/README.md) | [bob-cli-c9.3.1.1](bob-cli-c9.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2e08351`](https://github.com/bobs-org/bob-cli/commit/2e08351e893b59f79aa6de7f3c663db1000f640f) | feat(highlights): add force parser with reread/overwrite modes | [bob-cli-c9.3.1.1](bob-cli-c9.3.1.1.md) | 2026-10-25 16:22:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-c9.3.1.6.land--1][2] | Need descendant status, notes, and remaining follow-ups before closing bob-cli-c9.3.1 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md

<!-- sase:referenced-by:end -->
