# Sonar — Landing Page Content

Feed this into the Open Design visual build. One page; it is the hub — video and deck hang off it. Don't scatter links.

CCI voice throughout: problem-first, specific, no superlatives, no "excited to." See `BizDev/skills/brand-voice/cci-voice-guide.md`.

---

## Section 1 — Hero

**Headline (mixed weight — one emphasized phrase):**
Sonar — first-pass triage, **not a pitch generator.**

**Subhead:**
Paste a studio name or URL. Get one verdict and the response it calls for. Sonar decides — it never hands the question back.

**Primary CTA:**
→ `github.com/rocleemusic/sonar-operator`  
Label: "Get Sonar" or "Open repo"

---

## Section 2 — The three things it does

Plain language. Decisions, not features.

1. **Reads a prospect.** Studio name, URL, or inbound inquiry — scored against a 107-point fit framework and a live catalyst check.
2. **Returns one verdict.** PURSUE · NURTURE · DECLINE · FLAG. Every run. Not "here are some considerations."
3. **Drafts the response.** PURSUE gets an outreach email with the warm intro already named. NURTURE gets a watchlist entry with a single trigger to watch. DECLINE is brief, professional, done. FLAG surfaces the one question a human needs to call.

---

## Section 3 — The visible artifact (duel)

**Input label:** Input

```
Qualify Northwind Studios: indie action-adventure, no audio team,
no publisher deal, no raise announced.
```

| Generic AI | Sonar |
|---|---|
| "Northwind Studios looks like a strong fit. They're an indie action-adventure studio with an active team and a recent title. We recommend reaching out." | **DECLINE.** No funding from any source detected — publisher, raise, revenue, or grant. Can't hire on normal terms. Score: 58/107. |

*Sonar doesn't profile studios. It screens them.*

**[Embed video here — `sonar-duel-render.mp4` once hosted]**  
**[Link to deck — `sonar-deck/index.html` once hosted]**

---

## Section 4 — Who built it

I got into AI to get out of a spreadsheet.

Part of my job at a game-audio studio is finding studios worth working with — who's funded, who's in production, who hasn't hired an audio team yet — and scoring each one by hand. The scoring, the studios, the contacts were already in the workspace I keep every day. I just had to hand over the judgment I'd already been making.

*"Built by a game-audio studio's BD operator — I score these prospects by hand. Sonar is the spreadsheet, escaped."*

---

## Section 5 — Get it

**Repo:** `github.com/rocleemusic/sonar-operator`

**Setup — 3 steps:**
1. Create a project in Claude (claude.ai → Projects). Enable web search.
2. Add every file in the folder to the project's knowledge.
3. Set project instructions: *"Read identity.md and rules.md. You are Sonar. Decide, don't ask."*

Then paste: `Qualify [studio name]: [url]`

**Judge guide:** [link — `JUDGE_GUIDE.md` in Sonar repo]  
**Deck:** [link — `sonar-deck/index.html` hosted]

---

## Design notes for OD build

- Hub rule: video and deck **embed or link from this page**. One URL to share, not a scatter.
- Signal color (~5%): use `--cci-magenta` for the emphasized headline phrase and the DECLINE verdict in the duel.
- The duel table is the page's hero artifact — make it the visual anchor, not the founder section.
- No emoji. No em-dashes in rendered copy (use colons or commas per CCI style).
- Deck and video are secondary CTAs; the repo is the primary CTA.
