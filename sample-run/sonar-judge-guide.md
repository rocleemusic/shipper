# Judge Guide — Sonar × CCI

Notes to judges. Every entry is a falsifiable prompt — fire the input into Sonar, observe the output, check it against the Expect line. If the behavior doesn't match, the build failed its own claim. That falsifiability is the point.

## How to run

Open `sonar/rules.md` and `sonar/identity.md`. Feed both as the system prompt into any Claude session. Paste the prompt below. The operator should respond without asking clarifying questions — Sonar decides and drafts, or flags with the single question that resolves the ambiguity.

---

## 1. The core decision — DECLINE on a funding gap

**Fire:** `Qualify Pebblewick Games: 4-person bootstrapped mobile puzzle studio. No press, no raise, no publisher deal.`

**Expect:** `DECLINE`. Reason cites **"no identifiable funding from any source"** — not team size, not platform, not genre. Score appears (Tier 3 on fit, ~40/107), but rule 4 fires before the tier matters. Draft is brief and professional, not apologetic. No follow-up question.

**Why it matters:** Rule 4 is the funding filter. Sonar should surface the cited reason, not just the verdict — a DECLINE without a cause is a black box that can't be trusted.

---

## 2. The pursue path — mid-fit promoted by a live catalyst

**Fire:** `Qualify Lumen Hollow Games: ~40 staff, narrative-horror title, announced October ship date, seed-funded, no audio credits on their team page.`

**Expect:** `PURSUE · primary-vendor`. Rule 6 fires (Tier 2 + live catalyst). Score ~69/107. Outreach email leads with the ship date and the missing audio team — not a feature list. CCI credit cited matches the genre: *Starfield* or *The Outer Worlds 2*, not a sports title. "The in" is named if a CRM contact exists.

**Why it matters:** Proves the catalyst layer. Without the October ship date, this is NURTURE. With it, PURSUE. The rule that fired should be visible in the output — that's how a user audits the call.

---

## 3. The refusal — no fabrication on thin data

**Fire:** `Qualify Triton Reef Games — can't find them anywhere.`

**Expect:** `FLAG · not found`. Sonar names the exact gap: no studio matches the name or any URL. It asks the **one question** that resolves it ("Renamed, mis-spelled, or a sub-studio of a parent?"). It does not fabricate a score, a studio profile, or a guess. No verdict beyond FLAG.

**Why it matters:** The identity doc says "Missing data is a signal, not a guess." This is the hardest claim. A model that silently manufactures a studio and writes a PURSUE email fails the operator's core promise.

---

## 4. The edge case — studio closure → follow the person

**Fire:** `Re-triage Northwind Interactive. News says the studio shut down last week. We have Priya Anand (Audio Director) in our CRM, second-degree via Tom.`

**Expect:** Two decisions in one run. (a) `DECLINE` the *company* — studio closed, fit drops to 0, dead vendor target. (b) `NURTURE` the *person* — Priya Anand. Draft is a **warm check-in**, not a pitch: acknowledge the news, ask where she's landing, keep the door open. Closure named as a relationship catalyst. Flag that her next job change triggers a fresh re-triage.

**Why it matters:** This edge is in `rules.md` under Studio Closure. Good people scatter when studios close. Sonar should catch the pivot without being told — it's what separates an operator from a lookup tool.

---

## 5. The voice check — overflow nurture

**Fire:** `Qualify Tidewright Studios: ~80 staff, action game, one Sr Sound Designer on team page, small publisher, recently shipped their last title.`

**Expect:** `NURTURE · overflow angle`. Score ~59/107 — one point under the 60 overflow-pursue line; no fresh project catalyst. Watchlist entry names **one specific watch trigger** ("new project announcement or audio job post"). If a contact is `Overdue` in the CRM, a soft catch-up reason is noted alongside. Tone: direct and warm — no "excited to," no superlatives, no "reaching out to see if."

**Why it matters:** NURTURE is not a soft DECLINE — it's a positioned watch with a trigger. This also tests the overflow edge: the in-house audio lead is explicitly not a reason to DECLINE (rules.md, in-house audio edge).

---

## Bar

- [x] 5 prompts, each with Fire + Expect
- [x] Every Expect is checkable in one read — no "it should generally"
- [x] Two prompts target refusals: fabrication (3) and edge handling (4)
- [x] One targets voice + tone (5)
- [x] All four verdicts covered: PURSUE (2) · NURTURE (5) · DECLINE (1, 4a) · FLAG (3, 4a edge)

---

## Walkthrough — one full session

**Input:** `Qualify Northwind Studios: indie action-adventure, no audio team, no publisher deal, no raise announced.`

**What happens:**

1. Sonar reads the input against the scoring rubric (`reference/scoring-rubric.md`). Action-adventure scores high on genre (10). No audio team is an audio gap (22 points — the largest single cluster). But no funding from any source means rule 4 fires.

2. Score is computed — call it 58/107 — but the funding filter (rule 4) fires before the tier matters. No publisher, no raise, no revenue signal, no grant. "Can't hire on normal terms."

3. Verdict: `DECLINE`. Drafted artifact: a brief professional pass. No question handed back; the call is made.

4. MASTER-sheet record emitted: action first (DECLINE), score breakdown supporting. Pastes straight into column 15 of the target sheet.

**What a generic AI does with the same input:** Writes a confident outreach paragraph — "Northwind Studios looks like a strong fit. Indie action-adventure. Recommend reaching out." No rubric, no funding check, no reason cited.

**That's the product.** Sonar doesn't profile studios. It screens them.
