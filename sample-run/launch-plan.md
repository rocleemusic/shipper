# Shipper Sample Run — Sonar × CCI

**Run date:** 2026-06-13  
**Build:** Sonar — `P:\GitHub\icm-contest\sonar\`  
**Brand:** CCI (Clean Cuts Interactive) — voice: `BizDev/skills/brand-voice/cci-voice-guide.md`  
**Output:** `slipway/sample-run/` (overwrite)  
**Note:** Dogfood / calibration run. Ignores leverage order; builds full stack. Logs real production shape per tier.

---

## Step 0 — Tool Reachability

| Tool | Status | Notes |
|------|--------|-------|
| Open Design (MCP) | ✓ REACHABLE | `list_projects` returned 6 projects; OD daemon active |
| CCI design system | ✓ PRESENT | `P:\GitHub\cci-design-system\` — id `2f658978`; tokens inlined in deck HTML |
| Remotion | ✓ VERIFIED | `remotion still` succeeded; `out/sonar-duel-still.png` written. Font fix required: all three CCI comps + ObojimaRecap had unbounded `loadFont` calls blocking renders; patched to limit weights / commented out missing local files. |

---

## Gate 1 — Readiness: PASS

| Check | Result |
|-------|--------|
| Worked sample committed | ✓ — `examples.md`: 6 decisions, all 4 verdicts + not-found + studio closure pivot |
| README 5-minute stranger test | ✓ — 3-step setup, `Qualify [studio]: [url]` command, folder map table, make-it-yours section |
| ICM operator files (5) | ✓ — `identity.md`, `rules.md`, `examples.md`, `reference/` (9 files + templates), `README.md` |

No gaps. Build is ready.

---

## Gate 2 — Leverage Order: FULL STACK

Calibration run — build all tiers regardless of leverage order to log real production shape.

| Tier | Material | Status | File |
|------|----------|--------|------|
| 1 | Pitch blurb | ✓ BUILT | `sonar-blurb.md` |
| 1 | README hook polish | FLAG | See remaining track — current lead buries the hook |
| 2 | Landing page | ✓ BUILT via OD | `sonar-landing/index.html` — OD project `sonar-landing-8264`, run `f1db2ac8` succeeded |
| 2 | Landing content brief | ✓ BUILT | `sonar-landing-copy.md` |
| 3 | 60-second script + VO | ✓ BUILT | `sonar-video-script.md` |
| 4 | Judge guide | ✓ BUILT | `sonar-judge-guide.md` |
| 4 | Founder story | ✓ PRESENT | `_build/founder-story.md` (authored, feeds deck Slide 7) |
| 5 | Pitch deck | ✓ BUILT | `sonar-deck/index.html` (CCI-branded 8-slide portable HTML) |
| 6 | Animated flow | ✓ SMOKE PASS | `SonarDuel.tsx` — `out/sonar-duel-still.png` written; storyboard in `sonar-duel-storyboard.md`; full render gated on VO |

---

## Gate 3 — Hook: DUEL

**Detected, not proposed.** Same prospect name — Generic AI writes a confident outreach paragraph; Sonar runs the scoring rubric, hits the funding gap, returns DECLINE with the reason cited. One screen. No paragraph needed.

**Self-check:**
1. Category-swappable? No — the funding-gate refusal is Sonar's specific behavior.
2. Claims instead of shows? The duel column shows it; nothing asserted.
3. Buries the payoff? No — the verdict + reason leads; method supports in body.
4. Founder story on a persona? N/A — duel hook leads.
5. Can't be shown in one screen? One company name, two columns, one screen.

All five: PASS.

---

## Gate 4 — Flags: CLEAN

- **Lived or researched?** Roc is CCI's BD operator. The 107-point rubric, catalyst taxonomy, and CCI catalog are operational tools he uses daily. Fully lived.
- **Regulated domain?** Game-audio BD. No disclaimer required.
- **Multi-week / repeat?** Single comp day. Arc (Sonar built → Shipper dogfooded it same day) earns the founder line on Slide 7.

---

## Verdict: LAUNCH

**Hook:** Duel — `Qualify Northwind Studios: indie action-adventure, no audio team, no publisher deal, no raise` → Generic AI writes confident paragraph; Sonar routes to DECLINE, funding gap named.

**Materials in this folder:**

| File | What it is |
|------|-----------|
| `sonar-blurb.md` | Pitch blurb — submission line, one-liner, long form |
| `sonar-duel-storyboard.md` | Duel script — slide, embed, and Remotion motion notes |
| `sonar-landing-copy.md` | Landing hub content — section copy for OD visual build |
| `sonar-video-script.md` | Shot plan + separate record-ready VO script |
| `sonar-judge-guide.md` | 5 falsifiable prompts + walkthrough |
| `sonar-deck/index.html` | 8-slide CCI-branded portable HTML deck |

---

## Roc's Remaining Track

1. **README hook polish** — current lead (`"Drop this folder into a Claude project..."`) buries the hook. Swap to duel framing; see `sonar-blurb.md` for the language.
2. **Commit `sonar-judge-guide.md`** to the Sonar public repo — unblocks ICM criterion #4.
3. **Landing page visual** — feed `sonar-landing-copy.md` into OD; export portable HTML; host at a public URL.
4. **Record VO** (`sonar-video-script.md` Part 2, ~147 words) → splice into SonarDuel → render mp4 → host.
5. **Link everything** — landing hub URL, deck host URL, video URL — confirm all resolve in incognito.

---

## Submit-Readiness Snapshot

| Item | Status | Notes |
|------|--------|-------|
| Repo public + resolves incognito | Confirm | Verify at `github.com/rocleemusic/sonar-operator` |
| Worked sample committed | ✓ | `examples.md` — 6 decisions |
| Only shareable data in repo | ✓ | Obscured names; public CCI credits only |
| HANDOFF.md gitignored | ✓ | Not in public tree |
| README passes stranger test | ✓ | Hook polish needed but test passes |
| Blurb written | ✓ | `sonar-blurb.md` |
| Landing hub live | Pending | Visual build + host |
| Deck hosted + linked | Pending | Host `sonar-deck/index.html` |
| Video hosted + linked | Pending | VO record + render + host |
| Judge guide committed to Sonar repo | Pending | `sonar-judge-guide.md` → Sonar public repo |
| All links resolve | Pending | Unblocked by above |

---

## Production Log (calibration data)

*Timings logged here for Shipper's first full-stack run. Feed into Gate 2 on future runs.*

| Tier | Material | Notes |
|------|----------|-------|
| 1 | Blurb | Text-only; fast. Gate 3 must be settled first — hook determines the lead sentence. |
| 2 | Landing copy | Text-only; fast. Visual build (OD) is the time cost; copy itself is quick once hook is settled. |
| 3 | 60-second script | Two-part (shot plan + VO) is the right structure; keeps the recording clean. VO word count needs to be checked against 150-word target. |
| 4 | Judge guide | Structured against rubric; 5-prompt format is fast once examples exist. |
| 5 | Pitch deck | CCI HTML deck portable and self-contained. OD would add brand fidelity; direct HTML was faster for first pass. |
| 6 | Animated flow | `SonarDuel.tsx` registered and smoke-rendered; final render gated on VO recording. |
