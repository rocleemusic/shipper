# Duel Storyboard — Sonar × CCI

The strongest demo: same input, two columns. Proves the point instead of claiming it.

---

## Setup

**Input — shown once, centered:**

```
Qualify Northwind Studios: indie action-adventure, no audio team, no publisher deal, no raise announced.
```

This is a real checkable input. A judge can fire it into Sonar and get the same output.

---

## Left column — Generic AI

"Northwind Studios looks like a strong fit. They're an indie action-adventure studio with an active development team and a recent title. We recommend reaching out to explore a sound design partnership on their next project."

*Label: Generic AI*

---

## Right column — Sonar

**DECLINE.**

No funding from any source detected — publisher deal, raise, revenue signal, or grant. Can't hire on normal terms.

Score: 58/107 · funding 0 · audio gap 22 · genre 10 · active dev 12

*Label: Sonar*

---

## Payoff line

Sonar doesn't profile studios. It screens them.

---

## Layout notes

- Both columns: same width, same height. The contrast is the message — don't let Sonar's column sprawl.
- Generic AI: column border neutral (muted / gray). Sonar: magenta top accent.
- Verdict `DECLINE.` in `--cci-magenta`. Score line in `--cci-muted`.
- Payoff line: `--cci-lime`, centered below both columns.
- Input: centered above the grid, small label ("Input").

---

## Remotion motion notes (SonarDuel.tsx)

Duration: derive from `sonar-video-script.md` shot plan. 60s × 30fps = 1800 frames total. This scene covers 0–0:08 (0–240 frames).

| Frame range | What happens |
|---|---|
| 0–40 | Input text types in, centered. Both columns blank. |
| 40–140 | Generic AI column fills: paragraph types out at reading speed. |
| 90–150 | Sonar column: `DECLINE.` in magenta appears immediately. Generic AI keeps typing. |
| 150–210 | Sonar: reason text fades in. Score line appears. Generic AI paragraph still filling. |
| 210–240 | Hold. Payoff line fades in below the grid. |

**Motion principle:** Generic AI keeps going; Sonar stops. The stillness of the right column while the left fills is the point.

**Transition out:** at frame 240, fade both columns to 30% opacity; shot plan picks up with the next scene (score animation).

---

## Static export (Slide 3 / PDF thumbnail)

Use the same two-column layout frozen at the "hold" frame. Both columns fully visible. Payoff line visible. Works as the deck's comparison slide and as a PDF end-state still.

Check: truncate the generic AI paragraph to match Sonar column height — equal visual weight, stronger contrast.
