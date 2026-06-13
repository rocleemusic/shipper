# Shipper — Launch Pipeline Operator

Drop this folder into a Claude project and Shipper becomes a launch operator for a finished build. Tell it what you built, how much runway you have left, and who it's for. It decides whether the build is ready to ship, routes your effort to the highest-leverage launch materials, picks the hook, and drafts what it routes you to — or blocks you with a fix list if the build isn't ready yet.

## Setup
1. Create a project in Claude. Add every file in this folder to its knowledge.
2. Project instructions: *"Read identity.md and rules.md. You are Shipper. Run the four gates in order. Decide and draft; don't hand back a menu."*

## Use it
Paste: the repo (or a description), the runway you have left, the domain, and who it's for — plus a brand kit, or let it fall back to a neutral default.
Expect back: a readiness verdict, a leverage-ordered material plan, a chosen hook, and drafted materials — or a block naming exactly what to fix first. When the rendering tools (Open Design, Remotion, Canva) aren't reachable — e.g., running in the cloud — it hands you ready-to-paste prompts to produce each artifact, instead of the rendered files.

## What's in the folder
| File | Its one job |
|---|---|
| `identity.md` | Who Shipper is, what it owns, what it refuses |
| `rules.md` | The inputs + the four gates — readiness, leverage, hook, flags. The heart. |
| `examples.md` | Four decisions — edge cases + the hook-loop pause |
| `reference/winner-pattern-catalogue.md` | What actually wins, distilled from shipped launches |
| `reference/launch-tier-checklist.md` | The "done" bar for each launch material |
| `reference/hook-selection-rubric.md` | How to pick the lead hook + the weak-hook reject rules |
| `reference/brand-kit-schema.md` | The brand kit as input: schema, neutral default, voice pointer |
| `reference/tooling.md` | Route each artifact to a tool category; drive it or emit a prompt |
| `reference/tooling-profile.md` | The tool stack as a swappable input (default: this builder's) |
| `reference/judging-criteria.md` | The ICM 4 (default) + the notes-to-judges model |
| `reference/submit-readiness-checklist.md` | The final gate before submit |
| `reference/templates/` | Six skeletons: blurb, landing, 60s script (+ VO), judge guide, deck outline, duel storyboard |
