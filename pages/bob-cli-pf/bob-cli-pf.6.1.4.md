# Bead: bob-cli-pf.6.1.4 — Verify takeover restoration, keyboard access, and visual behavior

[Bead Pages](../README.md) / [bob-cli-pf.6.1](bob-cli-pf.6.1.md) / bob-cli-pf.6.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.md) · **Assignee:** `bob-cli-pf.6.1.4` · **Size:** medium
**Created:** 2026-11-23 20:38:15 EST
**Plan:** [202611/frontmatter\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:f4e751a976c731bafe5dbf7a | attached via sase artifact create --bead |

_Plus 12 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: build and run the disposable-vault real-Obsidian takeover matrix and offline wrapper, fix integration regressions, and retain inspected screenshots and reports tied to the exact CLI binary and plugin builds.

## Notes

[2026-11-24T11:29:49Z · bob-cli-pf.6.1.4] Recovered earlier work from landed plugin commits and transcript bob-cli-pf.6.1.4--p. The bead currently had no notes. Repeated NO-GO runs increased a nonexistent deferred-save wait from 360 to 480 to 600 seconds; each protected-note write occurred about 16 seconds after timeout. The harness later intentionally invokes native Add property for failed-opener-fallback on that protected note. Replaced this speculative wait with isolated native fallback on disposable 2026/20261117.md in a dedicated leaf, per-check timestamps and write-stage attribution. Also fixed ordinary editor screenshots to open the Bob property editor and require Add mode, and tightened sidebar presence/availability assertions. Focused ownership/spike/wrapper checks pass; full exact-build real-Obsidian acceptance and visual inspection remain. This remainder is bounded validation of the existing implementation, not a new implementation phase. No epic-symbol entries currently remain.

[2026-11-24T11:51:35Z · bob-cli-pf.6.1.4--1] Monitor g5645dfc9na3 proved protected-note bytes unchanged with no write transitions; remaining NO-GO was custom-shortcut-add-owned and sidebar-native. Isolated real Obsidian 1.15.1 diagnosis: closeEditor sent only one Escape from Add mode, leaving a browse modal whose scope intercepted the next shortcut. Cleanup now follows the existing menu/stage/filter/modal Escape ladder, observes dismissal, and fails if any modal persists. Sidebar probe used unregistered file-properties:open and matched All Properties; now invokes observed properties:open-local, targets only file-properties, reveals/loads its leaf, and requires visible usable native controls. Focused real-app checks for Mod+;, command dispatch, Alt+P, bank/ordinary native state and sidebar all pass on the unchanged production bundle. Fixed host test mocks to retain both adapter and shared coordinator listeners. 34 focused unit tests and build:check pass. Full matrix plus screenshot inspection still required; a monitored rerun also collects clean-HEAD controls for tracked n0 held-lock and km timing failures. No memory or production source changes.

[2026-11-24T12:08:32Z · bob-cli-pf.6.1.4--2] PROPOSED FOLLOW-UP: Existing bob-cli-n0 and bob-cli-km remain the only generic npm failures in monitor ghcg62vadrtz. npm-test.log records 9218/9220 unit tests and 26/26 perf tests passing; held-lock self-test reports exactly two commits instead of one, reproduced identically by clean-base-generic.log at clean bob-plugins e9d202c0ad46014082e9daa08246f92289180d01. The 200-link wall-clock assertion took 47.8 ms under full-suite load; its unchanged isolated file passes 23/23, and the clean-HEAD control also passes that timing node. These match the existing n0 deterministic failure and km load-sensitive flake. No new beads created; this phase remains open for visual acceptance only.

[2026-11-24T12:09:39Z · bob-cli-pf.6.1.4--2] Visual review rejected ghcg62 despite automated GO. Opened all 46 PNGs with image tools and verified every SHA256. Retained rejected report, individual visual verdicts, all images, logs and hash-matched original runner sources as file:explicit:f4e751a976c731bafe5dbf7a. Eleven images contain leaked metadata or native Properties below owned cards; eight day images crop the card after prior focus tests. Evidence-supported runner fixes isolate replaced-container DOM injection in a disposable tab (finally detach), require valid ownership/native visibility and a single metadata container before/after card captures, and reset screenshots to the card top with drawer closed. Focused real-Obsidian replacement + record/album/bank Reading probes pass; inspected their three diagnostic images as correct. 40 focused tests and build:check pass; final wrapper15/15. Production bundle remains unchanged. Full regenerated matrix and visual review remain required, so phase is not closed. No epic-symbol entries at this check.

## Dependencies

- **Depends on:** [bob-cli-pf.6.1.3](bob-cli-pf.6.1.3.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.6.1.5](bob-cli-pf.6.1.5.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.1.4.md) | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 29 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@beb821f`](https://github.com/bobs-org/bob-plugins/commit/beb821ff9395d73c64a9114445ef98fc086b1080) | test(property-cards): add frontmatter takeover e2e matrix | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-23 23:44:11 EST |
| bob-plugins | [`bob-plugins@8dab063`](https://github.com/bobs-org/bob-plugins/commit/8dab063f38fdbd665af38e12bbc5500ab84b0819) | test(property-cards): create the takeover profile before bob-control.json | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-23 23:52:17 EST |
| bob-plugins | [`bob-plugins@16e0767`](https://github.com/bobs-org/bob-plugins/commit/16e076756151608ee57591b505efac204216074a) | fix(ledger-tools): register Live Preview frontmatter ownership field | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 00:11:26 EST |
| bob-plugins | [`bob-plugins@dbc25c8`](https://github.com/bobs-org/bob-plugins/commit/dbc25c893e1c4bf7f6d9381080851589da124cd1) | fix(ledger-tools): register frontmatter ownership and harden real Obsidian verification | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 00:36:16 EST |
| bob-plugins | [`bob-plugins@28b3759`](https://github.com/bobs-org/bob-plugins/commit/28b3759436b2a7b432a7d6b04831553823571f3f) | test(ledger-tools): stabilize takeover cache restoration | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 00:55:23 EST |
| bob-plugins | [`bob-plugins@da80616`](https://github.com/bobs-org/bob-plugins/commit/da80616e1355d208eb35078b3e7e264edd95a559) | test(ledger-tools): stabilize StateField takeover cache harness | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 01:10:09 EST |
| bob-plugins | [`bob-plugins@dbc2f2c`](https://github.com/bobs-org/bob-plugins/commit/dbc2f2c2dc01a49d06c636e06f9ef3f157845605) | test(ledger-tools): stabilize StateField registration and stale-cache harness | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 01:26:41 EST |
| bob-plugins | [`bob-plugins@87a5f7e`](https://github.com/bobs-org/bob-plugins/commit/87a5f7e1ba443204de2f848bfa8c1517e13aba83) | test(ledger-tools): add stale-cache restoration diagnostics | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 01:44:23 EST |
| bob-plugins | [`bob-plugins@637c321`](https://github.com/bobs-org/bob-plugins/commit/637c3212617fa229996d2a81c140fcbf1cf76a2f) | test(ledger-tools): align stale-cache probe with restored summary | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 02:05:32 EST |
| bob-plugins | [`bob-plugins@d15f2a8`](https://github.com/bobs-org/bob-plugins/commit/d15f2a877e849dd0e32f52e771f4b9896906c6b1) | test(property-cards): isolate stale cache injection in takeover harness | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 02:24:23 EST |
| bob-plugins | [`bob-plugins@f319db7`](https://github.com/bobs-org/bob-plugins/commit/f319db7bd97f0724707b7f2c6f762507eb11039e) | test(ledger-tools): stabilize takeover matrix probes | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 02:39:56 EST |
| bob-plugins | [`bob-plugins@b476724`](https://github.com/bobs-org/bob-plugins/commit/b47672479d821c43ae5e843e08ed88779759c983) | test(ledger-tools): restore fixture after vim probe | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 02:51:20 EST |
| bob-plugins | [`bob-plugins@8a8b7a6`](https://github.com/bobs-org/bob-plugins/commit/8a8b7a642f64383d5300057b0972ee9d69c037c8) | fix(e2e): restore takeover fixture editor buffer | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 03:06:00 EST |
| bob-plugins | [`bob-plugins@d69f842`](https://github.com/bobs-org/bob-plugins/commit/d69f8423043a76ea4dd3c096ac626c5e566b8b8e) | test(frontmatter): trace takeover fixture byte transitions | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 03:18:32 EST |
| bob-plugins | [`bob-plugins@23f58cc`](https://github.com/bobs-org/bob-plugins/commit/23f58cc924a54bdb96caa56e8f342790ed66b534) | test(frontmatter): audit fixture writer attribution | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 03:33:53 EST |
| bob-plugins | [`bob-plugins@0a27756`](https://github.com/bobs-org/bob-plugins/commit/0a277566de3a1b0cae767fa6c55c1e676e168e5d) | fix(e2e): isolate Vim probe from fixture bytes | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 03:51:18 EST |
| bob-plugins | [`bob-plugins@545f734`](https://github.com/bobs-org/bob-plugins/commit/545f73491bcc424e64865c3cf55fd1207508af0f) | fix(e2e): isolate stale-cache probe from protected fixture | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 04:05:13 EST |
| bob-plugins | [`bob-plugins@784f2c4`](https://github.com/bobs-org/bob-plugins/commit/784f2c4f326e28ae32aacc79a600aca628b7b6df) | test: keep delayed Obsidian saves off protected fixture | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 04:24:13 EST |
| bob-plugins | [`bob-plugins@bbe2873`](https://github.com/bobs-org/bob-plugins/commit/bbe2873b059aae8dc41b63d4542bbd1ddc79ad7c) | test(frontmatter): keep deferred save on probe | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 04:35:40 EST |
| bob-plugins | [`bob-plugins@16da90a`](https://github.com/bobs-org/bob-plugins/commit/16da90a917df113c4effbfc7020acbc2513c75f8) | test(frontmatter): wait for deferred save on probe | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 04:49:48 EST |
| bob-plugins | [`bob-plugins@7290ae6`](https://github.com/bobs-org/bob-plugins/commit/7290ae65e2f65f2088c312d7e918b766c8a2a3de) | test: extend frontmatter takeover save wait | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 05:00:51 EST |
| bob-plugins | [`bob-plugins@29206e3`](https://github.com/bobs-org/bob-plugins/commit/29206e3265f6e41608484f39cbcaf4d746c4fe8a) | test(bob-ledger-tools): wait for delayed save before switching fixtures | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 05:13:09 EST |
| bob-plugins | [`bob-plugins@13f0320`](https://github.com/bobs-org/bob-plugins/commit/13f03206745bf6d377c88d0b9471b63918cbaecf) | fix(e2e): wait for delayed native save before protected fixtures | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 05:27:07 EST |
| bob-plugins | [`bob-plugins@b3e01d3`](https://github.com/bobs-org/bob-plugins/commit/b3e01d3653f17893529b1af8056b1c4ee0274970) | fix(e2e): wait for delayed native save before advancing fixture | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 05:41:23 EST |
| bob-plugins | [`bob-plugins@d51fed0`](https://github.com/bobs-org/bob-plugins/commit/d51fed05c4f5235aab49133b1d4023695b13a3ab) | test(obsidian): extend deferred save probe wait | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 05:57:10 EST |
| bob-plugins | [`bob-plugins@e9d202c`](https://github.com/bobs-org/bob-plugins/commit/e9d202c0ad46014082e9daa08246f92289180d01) | test(obsidian): extend frontmatter takeover save wait | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 06:14:46 EST |
| bob-plugins | [`bob-plugins@f3caac9`](https://github.com/bobs-org/bob-plugins/commit/f3caac9054a8e0a5718349f69f805dab59c12fc2) | test(frontmatter): isolate native fallback writes and tighten acceptance | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 06:32:20 EST |
| bob-plugins | [`bob-plugins@90e7809`](https://github.com/bobs-org/bob-plugins/commit/90e780905a07e059af2b54ad1c204e9d61d0f1d7) | test(frontmatter): dismiss editor layers and probe the native file sidebar | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 06:52:59 EST |
| bob-plugins | [`bob-plugins@f729388`](https://github.com/bobs-org/bob-plugins/commit/f729388375dcd946ac365d276cad25d1ccf99066) | test(frontmatter): isolate DOM injection and validate screenshot ownership | [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) | 2026-11-24 07:10:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.6.1.4--1][1] | Need phase scope and current status after xvfb failure | 3 |
| read-by | [agent:bob-cli-pf.6.1.4--2][1] | Review phase scope and status before resolving its real-Obsidian takeover matrix | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--3][1] | Review assigned phase scope and notes before updating its result | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--7][1] | Review phase scope and prior validation evidence before classifying the latest NO-GO and deciding whether this phase can close | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--8][1] | Inspect current phase notes and linked evidence before deciding whether this athena failure matches clean-base behavior | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--9][1] | Need the phase acceptance criteria, current notes, and clean-base comparison context before deciding whether this monitored run permits phase closeout. | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--a][1] | Check this phase's recorded clean-base comparison and latest matrix context before classifying the new NO-GO | 2 |
| read-by | [agent:bob-cli-pf.6.1.4--c][1] | Need assigned phase scope and history before updating its findings | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--f][1] | Review current phase findings and the recorded clean-base ownership failure before resolving this matrix run | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--h][1] | Need current phase status, completion criteria, and recorded notes before deciding whether to close | 1 |
| read-by | [agent:bob-cli-pf.6.1.4--n][1] | Need the assigned phase scope and existing notes before resolving this monitored E2E | 2 |
| read-by | [agent:bob-cli-pf.6.1.4--p][1] | Need phase state and notes before deciding whether this failed run can close the phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.1.4.md

<!-- sase:referenced-by:end -->
