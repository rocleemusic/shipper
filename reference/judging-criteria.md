# Judging Criteria

What the launch is graded against. This is an **input** — swap in the real rubric whenever one is published. The default is the **ICM 4**: the four criteria a folder-based operator is judged on, distilled from the ICM brief.

## The ICM 4 (default)
1. **It works for a real user, day one.** A real person in the domain could run this now and get value — not a demo that only works in the author's hands.
2. **The structure is actually defined.** Routing, handoffs, the decision logic — specific and inspectable, not hand-waved. For an operator: it **decides and routes a workflow end-to-end**; it isn't a chatbot with a system prompt.
3. **The README onboards a stranger.** Cold-readable in five minutes — no call with the author needed.
4. **The design decisions are real — and cited.** The choices are deliberate and explained where a judge can see them (README, `reference/`), each tied to something verifiable.

Comp #7 ("The Operator") sharpens #2: the build must decide and route, not answer questions. Shipper's gates already encode all four — Gate 1 guards #1 and #3, the operator's own rules guard #2, and auditability (judge guide, cited rules, a committed sample) guards #4.

## How Shipper uses them
Gate 2 routes effort toward whatever the criteria reward. Under the ICM 4 that means: a worked sample and a stranger-readable README **before** any video; a judge guide and cited rules **before** polish. If a published rubric weights something else, re-rank the leverage order against it.

## Notes-to-judges model (the judge guide)
Modeled on Mayston's `JUDGE_GUIDE.md`: every entry is a **falsifiable prompt** — *fire this exact input, expect this behavior.* Not "the system is robust," but "paste this thin input, watch it flag the gap instead of guessing." Falsifiability is the move — it lets a judge verify the headline claim cold, in minutes, and it's the most reliable converter to placement (winner-pattern #4). The `templates/judge-guide.md` skeleton builds one.
