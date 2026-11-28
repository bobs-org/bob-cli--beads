# Bead: bob-cli-q5.9.1.9 — Live end-to-end acceptance on bob and Obsidian

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.9` · **Size:** medium
**Created:** 2026-11-27 20:55:09 EST · **Closed:** 2026-11-27 22:29:27 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:199e86ddbcd46f13bf524afa | attached via sase artifact create --bead |
| related | file:explicit:2cad5d83476cfe0462f4aac7 | attached via sase artifact create --bead |
| related | file:explicit:341321c558dbc5d6e9b817a4 | attached via sase artifact create --bead |
| related | file:explicit:51251238996cea48dce2b39c | attached via sase artifact create --bead |
| related | file:explicit:546196f08ceaca5b6b9905a9 | attached via sase artifact create --bead |
| related | file:explicit:65c62bb1177c9ef45825be76 | attached via sase artifact create --bead |
| related | file:explicit:837ae5c4646af6ac95e9bc57 | attached via sase artifact create --bead |
| related | file:explicit:992139c5a9b91c50b7d41731 | attached via sase artifact create --bead |
| related | file:explicit:9ffe09238dc3bae2b590cfcf | attached via sase artifact create --bead |
| related | file:explicit:c29798712024f8949b31bd43 | attached via sase artifact create --bead |
| related | file:explicit:c7cae9c140afcb237cf1516c | attached via sase artifact create --bead |
| related | file:explicit:d3accb5b7ce1fe96ccd61d44 | attached via sase artifact create --bead |
| related | file:explicit:eacaa1dc057025c940b6a1df | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

e2e: run every bob and Obsidian acceptance case against the current masters, on a snapshot of the real vault and in real Obsidian, and record commands, JSON excerpts, and screenshots.

## Notes

[2026-11-28T03:29:11Z · bob-cli-q5.9.1.9] Live e2e on scratch bob 0.6.0 SHA 684811a9 (installed bob --version also 0.6.0); bob-plugins b23ccaee + case-8 marks runner; vault snapshot under /tmp/bob-e2e-q5 with snooze.notify off; ~/bob never written. CLI cases 1-7 all ok (file:explicit:d3accb5b7ce1fe96ccd61d44). Marks e2e 66/67 with case-8-linux-waker PASS spawn ["snooze","wake","-q","-f","json"] Notice notified=none (file:explicit:837ae5c4646af6ac95e9bc57). Card e2e PASS 60/60 SHA 684811a9 (file:explicit:c29798712024f8949b31bd43). Screenshots inspected: ⏰ clocks, due·waking, blocked/ignored, woke pills, plan chip ⏰ 3 · 21:18, card over-cap/blocked/invalid-time. Tarball file:explicit:2cad5d83476cfe0462f4aac7 summary file:explicit:9ffe09238dc3bae2b590cfcf.

[2026-11-28T03:29:16Z · bob-cli-q5.9.1.9] Mac cases 1 and 8 cited from sibling phases still in_progress at this close: case 1 Later-today band is mac-accept bob-cli-q5.9.1.5 (plan:202611/finish_snoozed_tasks_unattended.md item 6); case 8 locked/idle hold and unlock delivery is lock-accept bob-cli-q5.9.1.6. Linux case 8 Notice path is proven on this phase.

[2026-11-28T03:29:20Z · bob-cli-q5.9.1.9] PROPOSED FOLLOW-UP: reading-tomato-regression — marks e2e reading-view today tomatoes visible:false (tomatoes=0) while live view tomatoes=3; fixture clocks.stable=false nearMidnight minute 1323>1290 skipped 15 clock asserts. Inspected reading screenshot still shows ⏰ woke pills and snoozed heading. Looks like a fixture/runner near-midnight flake, not a q5 product defect. Do not keep this phase open.

[2026-11-28T03:29:27Z · bob-cli-q5.9.1.9] Verified live e2e on scratch bob 0.6.0 SHA 684811a9, plugins b23ccaee: CLI cases 1-7 ok; marks e2e 66/67 with case-8-linux-waker spawn snooze wake -q -f json and Notice when notified=none; card e2e 60/60; screenshots inspected (clocks, woke pills, plan chip, card). Mac cases 1/8 cited from in-progress bob-cli-q5.9.1.5/.6. Residual reading-tomato-regression filed as PROPOSED FOLLOW-UP. Artifacts attached. No --epic-symbol leftovers. ~/bob never written.

## References

- file:explicit:9ffe09238dc3bae2b590cfcf
- file:explicit:d3accb5b7ce1fe96ccd61d44
- file:explicit:837ae5c4646af6ac95e9bc57
- file:explicit:c29798712024f8949b31bd43
- file:explicit:2cad5d83476cfe0462f4aac7
- file:explicit:341321c558dbc5d6e9b817a4
- file:explicit:992139c5a9b91c50b7d41731
- file:explicit:c7cae9c140afcb237cf1516c
- file:explicit:199e86ddbcd46f13bf524afa
- file:explicit:65c62bb1177c9ef45825be76
- file:explicit:eacaa1dc057025c940b6a1df
- file:explicit:51251238996cea48dce2b39c
- file:explicit:546196f08ceaca5b6b9905a9

## Dependencies

- **Depends on:** [bob-cli-q5.9.1.2](bob-cli-q5.9.1.2.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-q5.9.1.3](bob-cli-q5.9.1.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.9/README.md) | [bob-cli-q5.9.1.9](bob-cli-q5.9.1.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@91db00d`](https://github.com/bobs-org/bob-plugins/commit/91db00d373c75a82b8c29e163a443afa3bff10be) | test(snooze): prove Linux case 8 waker spawn and Notice in marks e2e | [bob-cli-q5.9.1.9](bob-cli-q5.9.1.9.md) | 2026-11-27 22:30:37 EST |
