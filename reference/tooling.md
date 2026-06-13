# Tooling — route each artifact, drive the tool or emit the prompt

Shipper decides; the builder (or a downstream agent) produces. This routes each material to a tool *category* and says how to hand it off. The actual tools are an **input** — the tooling profile (`reference/tooling-profile.md`), swappable like the brand kit. This file is the generic logic; the profile holds the concrete bindings.

Rule of thumb: **write text directly, render pages and decks through a design tool, animate in a motion tool.**

## Route by category
| Material | Category | Output |
|---|---|---|
| Blurb · README · judge guide · founder story · VO script | **Direct** — Shipper writes it | markdown, paste-ready |
| Deck outline · duel storyboard | **Direct** — a plan that *feeds* a visual tool | markdown (not the finished artifact) |
| Landing page (the hub) · pitch deck | **Design tool** | portable HTML / slides |
| Animated flow · 60-second video (final) | **Motion tool** (HTML for a light embed) | rendered segment / video |
| Live demo | **The build's own frontend** | Shipper routes to it; it doesn't build it |

The profile binds each category to a real tool (a design tool = Open Design, say). Swap the profile and the categories don't move.

## Two modes — drive, or emit the prompt
Before driving anything, run the profile's **reachability check** for that tool. Then:

- **Reachable:** drive it per the profile's "how to invoke."
- **Not reachable — or no profile at all (e.g., Shipper in the cloud):** don't fake the artifact and don't stop. **Emit a ready-to-paste prompt** instead — Shipper's job becomes producing the prompt that a human, or an agent with tool access, runs. Emitting needs no local tools, so it's the universal fallback.

A good emitted prompt carries, every time:
- **The artifact spec** — the matching template, filled in.
- **The brand kit inline** — colors, fonts, motif, shape. Don't assume the downstream tool can read the kit file.
- **The voice** — the pointer's rules, inlined when the downstream context can't open the file.
- **The tool framing** — the target and its input shape from the profile, or the *category* if there's no profile: "Build as portable HTML for a design tool linked to design system …," "Write a motion composition that …."

Same artifact, two delivery modes. Gate 2 (which materials) and the templates (the spec) don't change — only whether Shipper renders it or hands off the prompt to render it.

## The boundary Shipper holds
Generation is automated and self-checked — on the rendered HTML, the comp code, the still, the render succeeding. **Motion and final taste are the builder's eye at the end.** Shipper produces and self-QAs; it doesn't sign off on feel.
