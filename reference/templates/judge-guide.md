# Template — Judge Guide

The notes-to-judges doc. Modeled on Mayston's: every entry is a **falsifiable prompt** — fire this exact input, expect this behavior. It lets a judge verify the claim cold, in minutes, without trusting the README.

## How to use it
Paste each prompt into the operator. The "Expect" line says what a correct response looks like — if you don't see it, the build failed its own claim. That falsifiability is the point.

## Entries (3–5)
**1. The core decision**
- **Fire:** [a real input that should produce the headline behavior]
- **Expect:** [the specific verdict / action + that it cites its reason]
- **Why it matters:** [the rule this proves]

**2. The refusal**
- **Fire:** [an input that should trip the operator's hard "no"]
- **Expect:** [it refuses / flags rather than fabricating]

**3. The edge case**
- **Fire:** [ambiguous or thin input]
- **Expect:** [it flags the specific gap, doesn't guess]

**4. (optional) The brand / voice check**
- **Fire:** [ask for an output artifact]
- **Expect:** [it reads in the brand voice — no hype, on-template]

## Bar
- [ ] 3–5 prompts, each with Fire + Expect.
- [ ] Every Expect is checkable in one read — no "it should generally…".
- [ ] At least one prompt targets a refusal (the operator's signature).
