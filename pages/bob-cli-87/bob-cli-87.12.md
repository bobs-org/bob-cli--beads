# Bead: bob-cli-87.12 — Mac acceptance and the real Highlights round trip

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.12` · **Size:** medium
**Created:** 2026-10-16 07:13:19 EDT · **Closed:** 2026-10-17 09:38:03 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

mac-acceptance: deploy to the Mac and run the corpus gate under BasicTeX and the PDFKit probe. Run Bryan's real Highlights round trip, record the verified results in docs, and write the decision record if it was approved.

## Notes

[2026-10-16T23:17:33Z · bob-cli-87.12] Bryan answered Mac-is-online at ~19:08 EDT, but Tailscale still shows kellys-macbook-pro Offline (last seen 2026-10-16T23:10:00Z). SSH to mac timed out after retries. Waiting for the lid to stay open and Tailscale to come back, then continuing install/doctor/corpus/PDFKit/snapshot.

[2026-10-16T23:41:11Z · bob-cli-87.12--2] Mac wait monitor 303cqwqkbew5 exited 1 after 16m49s: MAC_STILL_OFFLINE. 36 SSH tries all timed out. Tailscale kellys-macbook-pro last seen ~19:30 EDT then Offline; SSH still times out at 19:39 EDT. Asking Bryan again to leave lid open, plugged in, caffeinate, Tailscale connected.

[2026-10-16T23:49:09Z · bob-cli-87.12--2] Bryan answered Mac-is-awake (lid open, plugged in, caffeinate, Tailscale connected). Immediate SSH still timed out; Tailscale kellys-macbook-pro is active via nyc relay but offline (last seen ~19:30 EDT, tx with rx 0). Polling SSH again for ~10 minutes.

[2026-10-17T00:11:18Z · bob-cli-87.12--2] Mac answered SSH at 19:58 EDT (inventory: bob 0.1.0, pandoc 3.11, XeTeX TeX Live 2026, HEAD f1b37e5). bob ref doctor hung; a second SSH for git pull timed out. Tailscale last seen ~19:58 EDT then offline again (nyc relay tx, rx 0). Asking Bryan to keep it awake on the tailnet.

[2026-10-17T00:21:41Z · bob-cli-87.12--2] Bryan answered Mac-is-stable (lid open, plugged in, caffeinate, Tailscale Connected). Immediate SSH from athena timed out. One earlier nested hop via apollo succeeded (APOLLO_TO_MAC_OK), then all retries failed. Tailscale: kellys-macbook-pro Offline (athena last seen ~20:00 EDT, rx stalled; apollo last seen ~3m then frozen rx 16508, nyc relay tx climbing). ping, IPv4/IPv6 SSH, tailscale ssh, and nc :22 all timed out. Asking Bryan to Disconnect/Connect Tailscale, keep caffeinate -dims, Remote Login on, and confirm tailscale ping athena succeeds.

[2026-10-17T00:25:37Z · bob-cli-87.12--2] Bryan answered Mac-is-reachable (Tailscale toggled, caffeinate -dims, Remote Login, ping athena). Immediate probes still fail: ping/nc/:22/IPv4/tailscale-ssh/nested-apollo all timeout. Athena: kellys-macbook-pro active nyc-relay offline last seen ~24m, tx 20540 rx 2396. Apollo: last seen ~8m, tx 53108 rx 16508. Polling SSH again; if it comes up, run install+gate in one keepalive session.

[2026-10-17T00:28:42Z · bob-cli-87.12--2] Bryan answered Mac-is-reachable (toggle/caffeinate/Remote Login/ping athena). Immediate probes still fail: athena last seen ~28m; apollo nyc-relay tx with rx 0 last seen ~11m; tailscale ping from both times out; SSH/ping/nc/:22/IPv4/tailscale-ssh/nested-apollo all timeout. Asking Bryan to Quit Tailscale (not only Disconnect), confirm tailscale ping -c 5 athena pongs on the Mac, keep caffeinate -dims, and stay at the machine.

[2026-10-17T00:37:22Z · bob-cli-87.12--2] Bryan answered Ping-succeeded (Q3). Immediate inbound still fails: athena LastSeen ~20:30 EDT then Online=false Active=true Rx=0 Tx=4524 nyc relay; IPv4/IPv6 SSH, nc :22, tailscale ping, tailscale ssh, nested apollo all timeout. Asking Bryan to open ssh -N -R 2222:127.0.0.1:22 athena (outbound reverse tunnel) and keep caffeinate -dims running.

[2026-10-17T00:44:43Z · bob-cli-87.12--2] Bryan answered Tunnel-is-up (Q4). Immediate check: 127.0.0.1:2222 connection refused (no listener). Athena sshd is Port 34857, not 22, so the silent ssh -N -R ... athena likely hung on port 22 and looked like a live -N session. Direct/IP/apollo/tailscale-ping still timeout. Mac Online=false Active=true LastSeen ~20:30 EDT nyc relay Rx=504 Tx=9548. Asking for ssh -p 34857 with TUNNEL_OK echo and ExitOnForwardFailure.

[2026-10-17T00:52:46Z · bob-cli-87.12--2] Bryan answered TUNNEL_OK (Q5). Immediate check: no listener on 2222 on athena or apollo, no sleep 3600. Mac still Offline on athena. Apollo has a live SSH from 100.108.201.99 into tmux sase; inbound to the Mac still times out. Q5 was a false positive. Posted ~C / apollo reverse-tunnel instructions into that tmux session and polling 2222.

[2026-10-17T01:03:32Z · bob-cli-87.12--2] Q6 ~C reverse-forward was another false positive: Mac→apollo SSH logged out 20:57 EDT (session 20:32–20:57); no listener on apollo:2222 or athena:2222; inbound SSH still times out; Tailscale kellys-macbook-pro Offline last seen ~20:30 EDT. Asking Bryan to run a LOCAL (not tmux) ssh -R 2222 to apollo that prints TUNNEL_OK and sleep 3600.

[2026-10-17T01:11:10Z · bob-cli-87.12--2] Mac SSH live on LAN (direct 192.168.1.180). Deployed df4e120 via git pull --ff-only + just install + bob plugins sync. doctor completed: latex_packages warn missing titlesec.sty, enumitem.sty, lastpage.sty. Gating documented tlmgr --usermode install of those three. Other doctor fails (bob_xlib_pull, sidecars, listen sase) are pre-existing and out of this phase.

[2026-10-17T11:20:34Z · bob-cli-87.12] Mac is reachable on LAN 192.168.1.180 (kellys-macbook-pro active, direct). Checkout /Users/bbugyi/projects/github/bobs-org/bob-cli is df4e120, matching origin/master; bob 0.1.0 from that path, pandoc 3.11, XeTeX TeX Live 2026 BasicTeX. doctor still latex_packages warn missing titlesec.sty, enumitem.sty, lastpage.sty (fancyhdr/refcount/xurl present; user tree already inited at ~/Library/texmf). Previous tlmgr gate custom-2f6e5ed6 timed out overnight. Plugins dry-run up to date. Copied pdfkit_probe.swift to /tmp/pdfkit_probe.swift. Re-gating documented user-mode tlmgr install of the three missing packages; corpus gate, PDFKit probe, Highlights round trip, and docs remain after install.

[2026-10-17T11:46:35Z · bob-cli-87.12--1] Gate custom-8c1286c4 answered install but failed: POSIX sh printf %q invalid directive, so bash -lc got no argument. kpsewhich still missing titlesec.sty enumitem.sty lastpage.sty as of 2026-10-17 07:44 EDT. Re-gating quoting-safe python+ssh bash -s retry of the same user-mode tlmgr install; will not install silently.

[2026-10-17T12:04:49Z · bob-cli-87.12--2] Gate custom-0d798ba5 answered install; tlmgr --usermode installed titlesec/enumitem/lastpage then the gate script failed on bash printf --. Confirmed 2026-10-17 08:05 EDT: kpsewhich finds all three .sty under ~/Library/texmf; tlmgr --usermode reports installed; bob ref doctor latex_packages: ok (30 checked). Continuing corpus gate; will not re-install.

[2026-10-17T12:26:48Z · bob-cli-87.12--3] Mac corpus gate PASS 2026-10-17 08:23 EDT: 101 renders, 5062 dry-runs, 0 render/dry-run failures, 0 missing glyphs, 0 Type 3, 0 overfull, vault git unchanged. Output mac:/tmp/bob-note-snap-out. Unresolved-ref warnings in dry runs: 9580; parent fallbacks: 4347 (route: body). Continuing PDFKit probe and Highlights round trip.

[2026-10-17T12:35:51Z · bob-cli-87.12--3] PDFKit corpus probe PASS: 101/101 paired via workdir projected.md; 240 unknown tokens, 0 unexplained (207 In-this-note chrome, 29 return-link tag joins, 3 areas + 1 acegui wikilink-suffix joins). Chat-profile throwaway: unknown=1 Contents (TOC), 0 hyphen splits, 0 ligatures. In-vault lib/chat/bob_ref_reference_library_migration.pdf is pre-rule (20 hyphenation splits, 0 ligatures).

[2026-10-17T12:35:54Z · bob-cli-87.12--3] sase_blog round trip started: bob ref create sase_blog + scan landed lib/notes/sase_blog_261017.pdf (6 pages, title SASE Blog · 2026-10-17) and ref/notes/sase_blog_261017.md with source_note [[sase_blog]] parent [[sase_blog]]. Opened in Highlights.app. PDF has 13 obsidian:// URIs and 0 highlights://. Asking Bryan to highlight a task, prose, and image, add one #task comment, then sync.

[2026-10-17T12:35:58Z · bob-cli-87.12--3] PROPOSED FOLLOW-UP: Record decisions-web strand annotated-pdfs-render-on-xelatex — Highlights-bound PDFs bob renders (note snapshots and research reports) use pandoc + xelatex with the text-layer rule (ragged-right, no hyphenation, Ligatures=NoCommon) and never Chromium/Skia with variable fonts; note snapshots are dated reading projections, not prints. Rejected: Chromium; Typst now; Lua-side Bob parsing. Evidence: this epic plus Mac PDFKit probe 2026-10-17. decision_record=no on bob-cli-87 so this phase must not write the memory note.

[2026-10-17T12:47:58Z · bob-cli-87.12--3] Round-trip verify after Bryan Done: Highlights still has sase_blog_261017.pdf open. File Save wrote lib/notes/sase_blog_261017.md sidecar containing only the page-1 marker (highlights_count 0). PDF has 0 /Highlight annots; bob ref sync --dry-run annotation_tasks_create 0; sase_blog.md has no new follow-up task. Asking Bryan to highlight a task line, prose, and an image, add a #task comment, Save, then bob ref sync.

[2026-10-17T12:58:22Z · bob-cli-87.12--3] Round-trip still empty after Bryan Done (Q1): Highlights Notes panel on sase_blog_261017.pdf shows only the page-1 marker; sidecar 268 bytes; highlights_count 0; PDF /Contents is the marker only; no textbundle. Asking again with Notes-panel + wc -c checks. Corpus gate and PDFKit remain PASS.

[2026-10-17T13:07:24Z · bob-cli-87.12--3] Round-trip still empty after Bryan Done (Q2): AX Notes panel on sase_blog_261017.pdf (correct tab selected, Highlight tool already on) still only the page-1 marker; sidecar 268 bytes mtime 08:44; PDF /Highlight=0; highlights_count 0; no textbundle. Asking again with Mac-keyboard steps and wc -c gate. Corpus gate and PDFKit remain PASS.

[2026-10-17T13:18:55Z · bob-cli-87.12--3] Round-trip still empty after Bryan Done (Q3): sidecar lib/notes/sase_blog_261017.md still 268 bytes mtime 08:44; highlights_count 0; PDF /Highlight=0; no textbundle; sase_blog.md has no annotation follow-up. Q3 claimed wc -c > 268; measured 268. Highlights was on the sase_blog_261016 tab (page 4) when activated; reopened sase_blog_261017 (page 1 of 6), Highlight tool selected, Notes panel visible. Corpus gate and PDFKit remain PASS. Asking again at the Mac keyboard.

[2026-10-17T13:28:45Z · bob-cli-87.12--3] Round-trip still empty after Bryan Done (Q4): sidecar lib/notes/sase_blog_261017.md still 268 bytes mtime 08:44; highlights_count 0; PDF /Highlight=0; no textbundle. Q4 cl

… and 324 more characters

## Dependencies

- **Depends on:** [bob-cli-87.10](bob-cli-87.10.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.11](bob-cli-87.11.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.8](bob-cli-87.8.md) ✓ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.9](bob-cli-87.9.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.12.md) | [bob-cli-87.12](bob-cli-87.12.md) | 0 |
