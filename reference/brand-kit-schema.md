# Brand Kit Schema

Shipper styles every artifact from a brand kit. The kit is an **input** — Shipper never invents one.

- **Provided** → use it.
- **None** → fall back to the neutral default below, and say so in the plan.
- **Asked to set one up** → emit the fillable schema for the builder to complete, then use it.

The kit mirrors the RDS token structure (colors, fonts, motif, shape) with one field that does the heavy lifting: **voice is a `.md` pointer**, not prose. Copy lives or dies on voice, and voice doesn't fit in a token.

## The schema (fill this in)
```yaml
brand:
  name:                              # e.g. "Roc Does Sound"
  colors:
    base:                            # the canvas (paper / dark). ~70% of any surface.
    ink:                             # headlines, dark sections.
    signal:                          # the ONE accent. ~5% of a surface. Never a background.
    support:                         # 1–2 quiet supporting tones (body, borders).
  fonts:
    display:                         # headline face + weight
    body:                            # body / UI face + weight
    mono:                            # code / captions (optional)
  voice:   ./path/to/voice-rules.md  # a POINTER to a voice doc, not prose
  motif:                             # the one brand graphic, in a line (e.g. "Fletcher–Munson curve")
  shape:                             # corner radius + feel (e.g. "near-square, 2–4px radii")
```

## Rules that travel with the kit
- **Signal color is ~5% of a surface.** If the accent is everywhere it stops meaning anything. Roughly 70% base, 25% support, 5% signal.
- **One emphasized phrase per headline.** Mixed-weight: a headline is a sentence with exactly one word or phrase carrying the emphasis. If two compete, the line is wrong.
- **Voice is the pointer, not a vibe.** Every line of copy is checked against the doc the pointer names. Swap the pointer, swap the voice — nothing else changes.
- **No emoji** unless the voice doc explicitly allows them.

## Neutral default (when no kit is supplied)
Enough to produce clean, unbranded artifacts without guessing at someone's brand.
```yaml
brand:
  name:    (the build's name)
  colors:
    base:    "#0E0F13"   # near-black
    ink:     "#F5F5F4"   # off-white
    signal:  "#3B82F6"   # one blue accent, used sparingly
    support: "#9CA3AF"   # neutral grey
  fonts:
    display: "Inter, 600"
    body:    "Inter, 400"
    mono:    "JetBrains Mono"
  voice:   (inline) plain, direct, specific — short sentences, concrete nouns, no hype, no emoji
  motif:   none
  shape:   "6px radii, neutral"
```
The default's voice is the inline rules above — it carries no voice doc, because there's no brand to point at yet. A real kit always points at one. When Shipper runs on the default, it says so: a neutral kit is a fallback, not a recommendation. Supplying a real kit is always the stronger launch.
