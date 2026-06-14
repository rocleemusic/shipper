# Tooling Profile

The tool stack Shipper produces through — an **input**, swappable like the brand kit. The generic routing lives in `tooling.md`; this binds each tool *category* to a real tool, says how to invoke it, and how to check it's reachable.

- **Provided** → bind to it.
- **None, or a tool is unreachable** → Shipper emits ready-to-paste prompts instead (the universal fallback; see `tooling.md`).

Each binding answers three things: **what** the tool is, **how to invoke/feed** it, and the **reachability check** Shipper runs before driving it.

## The schema (fill this in)
```yaml
profile:
  name:                      # e.g. "Roc Does Sound — local stack"
  design_tool:               # pages + decks → portable HTML / slides
    tool:
    invoke:                  # how Shipper drives it
    reachable_when:          # the check Shipper runs first
  motion_tool:               # animated flow + final video
    tool:
    invoke:
    reachable_when:
  deck_tool:                 # optional; only if the deck tool differs from the design tool
    tool:
    invoke:
    reachable_when:
  direct:                    # text — no tool
    tool: none
```

## Default profile — this builder's stack (Roc Does Sound)
- **Design tool → Open Design (MCP).**
  - *Invoke:* create a **new project** for each artifact (landing page, deck) — never the design system project itself, which is a source of tokens, not an artifact home. Link the design system via its CSS path or `designSystemId`. Use `start_run` with an artifact brief to drive OD's generative layer; pull the result with `get_artifact`. Output is **portable HTML**, not locked to OD. Build the design system *first*; never freehand a branded artifact.
  - *Reachable when:* the OD daemon responds (`list_projects`).
  - The `user:` id is this profile's pointer to wherever the **brand kit** is registered in OD — the one place brand and tooling meet.
- **Motion tool → Remotion.**
  - *Invoke:* compositions live in `my-animations/animation-studio`. Write the comp, render via CLI, self-QA with a `remotion still` PNG before a full render. The brand ports in once (RDS→Remotion tokens). Splice the recorded VO via Remotion audio or ffmpeg.
  - *Windows invocation:* the default `npm run still` OOMs on large comps. Use PowerShell: `$env:NODE_OPTIONS="--max-old-space-size=4096"; .\node_modules\.bin\remotion.cmd still builds/index.ts --public-dir ./builds/public [CompId] [out.png] --frame=0`
  - *Permission check (run before the smoke render):* read `.claude/settings.json` and check whether `node_modules\.bin\remotion.cmd` (or equivalent) is in the allow list. If it is not present → **stop and prompt:** "The Remotion smoke render requires `node_modules\.bin\remotion.cmd` to be pre-approved. Add it to `.claude/settings.json` → `permissions.allow`, then re-run." Do not attempt the render without it.
  - *Reachable when:* Remotion is installed in `my-animations/animation-studio` AND the permission check passes. **Step 0 of any video run:** permission check → resolve the path junction → one-frame smoke render.
- **Deck tool → Open Design** (slide archetypes from the outline), **or Canva (MCP)** when a Canva brand template exists — feed the deck-outline's per-slide fields into the template. Otherwise prefer OD and treat Canva as an export target.
- **Direct → none.** Text artifacts need no tool; Shipper writes them in the brand voice and the builder pastes them where they go.

## Swapping the profile
Replace the bindings above with your own — Figma + After Effects, v0 + a video editor, plain prompts, whatever you run. The categories in `tooling.md` don't change; only what they point to. Supply nothing and Shipper emits prompts framed by category, for you to run wherever you like.
