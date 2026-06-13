# Shipper Sample Run — Sonar × CCI

**Run date:** 2026-06-13 (post-submission)  
**Build:** Sonar (shipped, https://github.com/rocleemusic/sonar-operator)  
**Brand:** CCI (Clean Cuts Interactive)  
**Audience:** comp judges + studios evaluating CCI's BD approach

---

## Step 0 — Tool Reachability

| Tool | Status | Notes |
|------|--------|-------|
| Open Design daemon | ✓ REACHABLE | `cci-design-system` project loaded (id `2f658978`, succeeded) |
| CCI design system in OD | ✓ PRESENT | Prototype project at `P:\GitHub\cci-design-system\`. Not registered as `user:` id — deck links `styles.css` directly (BUILD-LOG option b). |
| Remotion | ✓ REACHABLE | `P:\GitHub\RL_MAP\RL_MAP\my-animations\animation-studio`. v4.0.448. CCI compositions already registered. Smoke render passed (`CCILowerThird`, frame 0). |

---

## Gate 1 — Readiness: PASS

- Worked sample: ✓ — `examples.md`, 6 worked decisions (all 4 verdicts + not-found failure), committed to public repo
- README stranger test: ✓ — setup in 3 steps, one-command use (`Qualify [studio]: [url]`), folder map, make-it-yours, roadmap
- 5 ICM files: ✓ — `identity.md`, `rules.md`, `examples.md`, `reference/` (9 files + templates), `README.md`; all present and functional

No gaps.

---

## Gate 2 — Leverage Order: route to remaining stack

Already shipped pre-noon: pitch blurb · CCI landing page (Sonar CCI landing via OD-CCI)

Remaining (calibration run — full stack):
1. **Pitch deck** — 8 slides, OD-CCI → BUILD ✓
2. **60-second shot plan + separate VO script** — BUILD ✓
3. **Remotion duel comp** — `SonarDuel.tsx` → BUILD ✓

---

## Gate 3 — Hook: DUEL. No PAUSE.

**Detected, not proposed.** Same prospect name — two AIs. Generic AI writes a confident outreach paragraph. Sonar refuses to profile and routes instead: runs the scoring rubric, finds the funding gap, returns DECLINE with the reason. The refusal is the product.

**Self-check (weak-hook rules):**
1. Category-swappable? No — only Sonar refuses to profile and routes.
2. Claims instead of shows? The duel column shows the behavior; nothing asserted.
3. Buries the payoff? No — the behavior split leads, method supports in body.
4. Founder story on persona? N/A — duel hook.
5. Needs a paragraph to land? One company name, two columns — one screen.

**All five rules: PASS.**

---

## Gate 4 — Flags: CLEAN

- Lived or researched? Roc is CCI's BD operator. Fully lived.
- Regulated domain? Game-audio BD. No disclaimer required.
- Multi-week/repeat? Single comp day. Arc (built Sonar + Shipper dogfooded it same day) → earns the founder line in Slide 7.

---

## Plan

**Verdict:** LAUNCH

**Hook:** Duel — `Qualify Northwind Studios` → generic AI writes a confident profile; Sonar routes to DECLINE with the funding gap named.

**Materials (in build order):**
1. `sonar-deck/index.html` — CCI-branded 8-slide portable HTML deck (built, in this folder)
2. `sonar-video-script.md` — shot plan + separate record-ready VO script (built, in this folder)
3. `SonarDuel.tsx` — Remotion comp registered in the animation-studio; render via `npx remotion render builds/index.ts SonarDuel`; host the rendered mp4 (don't commit)

**Roc's remaining:** record the VO · review motion + final taste · host the rendered video + link it here.

---

## Phase 2 (v2) — 2026-06-13

**Run against:** Sonar (post-submission, same build)  
**What changed:** Tier 4 (walkthrough + judge guide + founder-story framing) was missing from the v1 calibration run. v2 fills it.

### Gate re-run (abbreviated — no changes since v1)

| Gate | Result |
|------|--------|
| Gate 1 — Readiness | PASS (unchanged) |
| Gate 2 — Leverage order | Tier 4 now due |
| Gate 3 — Hook | DUEL (unchanged) |
| Gate 4 — Flags | CLEAN (unchanged) |

### Artifact produced

**`sonar-judge-guide.md`** (this folder) — 5 falsifiable prompts covering all four verdicts + a walkthrough section. Modeled on the Mayston `JUDGE_GUIDE.md` format. Satisfies ICM 4 criterion #4 (design decisions are real and cited; a judge can verify cold).

### Submit-readiness check (Sonar × CCI launch materials)

| Item | Status | Notes |
|------|--------|-------|
| Sonar repo public | ✓ | https://github.com/rocleemusic/sonar-operator |
| Worked sample committed | ✓ | `examples.md` — 6 decisions, all 4 verdicts |
| Only shareable data | ✓ | Obscured names; CCI public credits only |
| HANDOFF.md gitignored | ✓ | Not in public tree |
| README — 5-min stranger test | ✓ | Setup in 3 steps, folder map, make-it-yours |
| Judge guide in Sonar repo | ✗ | `sonar-judge-guide.md` built here — **needs to be committed to Sonar repo** |
| Landing hub live | ✗ | Built via OD-CCI — URL not yet confirmed or linked here |
| Deck hosted + linked | ✗ | `sonar-deck/index.html` built — needs a host URL here |
| Video hosted + linked | ✗ | VO not yet recorded; no mp4 yet |
| All links resolve | ✗ | Blocked by the three items above |

### Remaining (Roc's track)

1. Commit `sonar-judge-guide.md` to the Sonar public repo — unblocks ICM criterion #4.
2. Confirm landing hub URL → link it here.
3. Host `sonar-deck/index.html` (OD export or CDN) → link it here.
4. Record VO (`sonar-video-script.md` Part 2, ~147 words) → splice into SonarDuel → host mp4 → link it here.
5. Motion + final taste review (Roc's eye).
6. Final pass: verify all links resolve in incognito before calling the launch kit done.
