# Bead: bob-cli-q5.8.1.6.4 — Fix the beacon glyph, record lifecycle, diagnostics, and docs

[Bead Pages](../README.md) / [bob-cli-q5.8.1.6](bob-cli-q5.8.1.6.md) / bob-cli-q5.8.1.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.land.md) · **Assignee:** `bob-cli-q5.8.1.6.4` · **Size:** medium
**Created:** 2026-11-26 20:05:50 EST · **Closed:** 2026-11-27 02:39:29 EST
**Plan:** [202611/mac\_snooze\_wake\_notice\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice_repair.md)

## Description

records-repair: keep the base status glyph template-tinted beside an amber alarm beacon, clear beacon and records on vault change, stop restores from re-posting records, isolate snooze diagnostics, finish the protocol and settings docs, and close the records test gaps.

## Notes

[2026-11-27T06:52:40Z · bob-cli-q5.8.1.6.4] PROPOSED FOLLOW-UP: Investigate the full-suite-only MeetingNotesSessionTests.testLateListCannotReplaceNewerChooserGeneration ordering failure; its isolated rerun passed, and existing task bob-cli-qk tracks the related out-of-order MeetingNotes preview race.

[2026-11-27T06:52:41Z · bob-cli-q5.8.1.6.4] PROPOSED FOLLOW-UP: Reconcile the baseline just docs-check failure at docs/reference/vault-format.md (6030/6000 words); this phase did not change that page and the existing task bob-cli-oc tracks the same overflow.

[2026-11-27T07:39:29Z · bob-cli-q5.8.1.6.4--2] Verified exact-SHA macOS CI passed: run 45957005662, snapshot SHA e443aa407410a1cc27dc35ef106c517fdafe3c6f (macOS 26 SwiftPM: lint, build, test, bundle/signature, launch smoke, install/reinstall all passed). sase bead epic-symbols reported no --epic-symbol entries. Local Mac targets remain unverified; scratch compile was unavailable because SSH to Mac timed out. Existing docs and portable-check follow-ups remain recorded.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.6.5](bob-cli-q5.8.1.6.5.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.4.md) | [bob-cli-q5.8.1.6.4](bob-cli-q5.8.1.6.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.6.3--2][1] | Check record-lifecycle bead owns beacon expiry failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.3.md

<!-- sase:referenced-by:end -->
