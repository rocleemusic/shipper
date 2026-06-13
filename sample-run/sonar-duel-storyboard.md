# SonarDuel — Storyboard v2

5-section arc, 1800 frames @ 30fps = 60s. Source: sonar-deck + _build/founder-story.md.
No VO dependency — animation self-contained.

---

## Section map

| # | Section | Global frames | Duration | Visual |
|---|---------|---------------|----------|--------|
| 1 | Problem | 0–180 | 6s | Three lines appear sequentially on dark field |
| 2 | Duel | 180–1080 | 30s | Split-screen. Input → generic types → DECLINE drops → reason → hold |
| 3 | Verdicts | 1080–1290 | 7s | Header + subhead + four cards staggered |
| 4 | Founder | 1290–1560 | 9s | Three-line personal beat |
| 5 | CTA | 1560–1800 | 8s | Centered: tagline → "Sonar." → URL |

---

## Phase constants

### Section 1 — Problem (local = global)

| Frame | Time | Event |
|-------|------|-------|
| 0 | 0s | "Studios hit your inbox every week." springs in |
| 40 | 1.3s | "Most aren't right." springs in |
| 80 | 2.7s | "Generic AI writes a confident paragraph about all of them anyway." |
| 180 | 6s | Section ends |

### Section 2 — Duel (local frame = global − 180)

| Local | Global | Time | Event |
|-------|--------|------|-------|
| 0 | 180 | 6s | Eyebrow "Same prompt. Two answers." + both column containers spring in |
| 60 | 240 | 8s | Input "Qualify Northwind Studios" fades in |
| 120 | 300 | 10s | Generic AI typing starts (~170 chars) |
| 480 | 660 | 22s | Typing done (360f = 12s = ~14 chars/sec — readable) |
| 540 | 720 | 24s | DECLINE springs in (spring, damping 10) |
| 600 | 780 | 26s | Reason types in (~90 chars) |
| 780 | 960 | 32s | Score line fades in (180f = 6s for reason = 15 chars/sec) |
| 810 | 990 | 33s | Payoff line: "Sonar doesn't profile studios. It screens them." |
| 900 | 1080 | 36s | Section ends |

### Section 3 — Verdicts (local frame = global − 1080)

| Local | Global | Time | Event |
|-------|--------|------|-------|
| 0 | 1080 | 36s | "One verdict, every time." + "First-pass triage, not a pitch generator." |
| 40 | 1120 | 37.3s | PURSUE card |
| 68 | 1148 | 38.3s | NURTURE card |
| 96 | 1176 | 39.2s | DECLINE card |
| 124 | 1204 | 40.1s | FLAG card |
| 210 | 1290 | 43s | Section ends |

### Section 4 — Founder (local frame = global − 1290)

| Local | Global | Time | Event |
|-------|--------|------|-------|
| 0 | 1290 | 43s | "I got into AI to get out of a spreadsheet." |
| 90 | 1380 | 46s | "The scoring, the studios — the judgment was already in my workspace." |
| 190 | 1480 | 49.3s | "I just handed it over." |
| 270 | 1560 | 52s | Section ends |

### Section 5 — CTA (local frame = global − 1560)

| Local | Global | Time | Event |
|-------|--------|------|-------|
| 0 | 1560 | 52s | "Drop it in a project. Start qualifying." |
| 30 | 1590 | 53s | "Sonar." in large white type |
| 70 | 1630 | 54.3s | github URL in magenta |
| 240 | 1800 | 60s | End |

---

## Smoke test frames

| Frame | Section | What you should see |
|-------|---------|---------------------|
| 90 | Problem | All three lines settled |
| 540 | Duel | Generic typing mid-paragraph, Sonar column empty |
| 900 | Duel | DECLINE, reason, score all settled; payoff line visible |
| 1140 | Verdicts | All four cards settled |
| 1410 | Founder | Two lines settled, third appearing |
| 1720 | CTA | All CTA elements settled |

---

## Layout notes

- Always-on: 4px magenta top bar, "Clean Cuts Interactive" footer bottom-left
- Generic AI column: neutral top border (`#3a3a3a`)
- Sonar column: magenta top border (`#ec008c`), always, even when empty
- DECLINE: `font-size: 24px`, `font-weight: 700`, magenta — spring with `damping: 10` for snap
- Payoff: lime (`#ccff00`), centered below both columns
- Verdict cards: left border magenta, 2×2 grid, staggered by 28 frames each
- Founder: left-aligned, intimate scale — headline 34px/700, body lines 22px/400
- CTA: centered, "Sonar." at 68px/700 white — repo URL 16px magenta below
