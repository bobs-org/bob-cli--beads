# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2 — Attach saved sources to the ambiguous and title-mismatched backfill skips

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2` · **Size:** medium
**Created:** 2026-10-27 06:23:58 EDT · **Closed:** 2026-10-27 06:54:34 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

## Description

attach-source-skips: resolve bob-cli-co per the attach_disambiguation decision by verifying every candidate of an ambiguous stem and running the write pass only through a Bryan-approved gate.

## Notes

[2026-10-27T10:54:28Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2] attach-source-skips done (verify branch): ambiguous stems now verify every candidate and attach only on exactly-one-pass; explicit REF -s FILE pairs skip the title check but still verify blocks; block-match thresholds unchanged. Added -f/--format json (pure-JSON envelope with per-row candidates, verdicts, matched/total). Files: src/native/ref_library/attach.rs, src/native/ref_library/cli.rs, tests/cli/ref_library/attach.rs (new: one-pass, zero-pass, two-pass, explicit-pair, JSON verdicts), docs/ref.md. Gates: just check exit 0 (fmt, clippy, full suite incl. 9 attach integration tests with real pandoc/xelatex/pdftotext; docs_reference golden ok; bob-docs check 447 passed). LIMITATION (for lander): no write pass ran — it needs a Bryan-approved /sase_gate turn. Read-only dry run on athena, 4 canonical research sidecars as -s: summary 38 attached, 262 skipped. Of the 47 old ambiguous stems, 36 now attach (1-of-N verified; plan-vs-report collisions resolve via title check) and 11 stay skipped (ambiguous: 0 of 2 verified). 35 title mismatches still need human-reviewed explicit pairs; pairing list (REF :: candidate FILE) extracted from -f json dry run, 35 lines in /tmp/attach-pairings.txt and /tmp/attach-dry.json on athena. Gate commands: (1) write pass: BOB_DIR=/home/bryan/bob bob ref attach-source -s <bob-cli research> -s <sase research> -s <actstat research> -s <tailnet research> (expect 1 revertable batch of 38); (2) per approved pair only: bob ref attach-source <REF> -s <FILE>. No PROPOSED FOLLOW-UP discovered.

[2026-10-27T10:54:34Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2] Verified: just check exit 0 (fmt, clippy, full cargo suite incl. 5 new attach tests green with real render toolchain); read-only dry run on athena over 4 research sidecars: 38 would attach (36 disambiguated 1-of-N, 2 single), 11 ambiguous 0-of-2 stay skipped, 35 title mismatches listed for review; no vault writes made, vault tree clean. Write pass left for a Bryan-approved gate turn per plan.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`69b7d96`](https://github.com/bobs-org/bob-cli/commit/69b7d96211d4106da89bd8cdb9cc622d3ae7e8db) | feat(ref): verify every attach-source candidate and attach on exactly-one-pass | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2.md) | 2026-10-27 06:56:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.2/README.md

<!-- sase:referenced-by:end -->
