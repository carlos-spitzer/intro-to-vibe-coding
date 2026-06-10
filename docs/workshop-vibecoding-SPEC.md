# SPEC (AS-BUILT) — Workshop "Intro to Vibe Coding"

> **Purpose of this document.** This is the single source of truth for the workshop, kept up to date with the actual delivered state of all materials. It serves two roles: (1) a planning reference for anyone facilitating the session, and (2) the document to attach to Claude Design when recreating or editing any material from scratch.
>
> **Status:** materials delivered as HTML, June 2026. GitHub repository and GitHub Pages site live. See §9 for open items.

---

## 0. Quick facts

| Field | As-built value |
|---|---|
| **Title** | Vibe coding — "From idea to prototype in a single session" |
| **Author / byline** | Carlos Spitzer |
| **Program** | Exec. Master, Digital Business, Innovation & Entrepreneurship (EMBDIE) |
| **Date stamp** | June 2026 |
| **Language** | English |
| **Duration** | 120 min |
| **Audience** | NON-technical profiles (business, strategy, entrepreneurship) |
| **Practice mode** | Browser + Claude account only (zero installation required) |
| **GitHub repo** | https://github.com/carlos-spitzer/intro-to-vibe-coding |
| **GitHub Pages** | https://carlos-spitzer.github.io/intro-to-vibe-coding |
| **Deliverables** | (1) Theory Deck — 22 slides · (2) Prompt Cheat Sheet — 1 page · (3) Student Handout — 3 pages · (4) GitHub Pages landing site |

---

## 1. Design system (as-built)

### Typography
| Role | Font |
|---|---|
| Display / headings | **Space Grotesk** |
| Body / UI | **Hanken Grotesk** |
| Code / prompts / terminal accents | **JetBrains Mono** |

### Color tokens (defined in OKLCH, not hex)
```
--ink:        oklch(0.22 0.02 292)    /* near-black, slight violet */
--paper:      oklch(0.975 0.006 85)   /* warm off-white background */
--white:      oklch(0.995 0.003 85)
--grey:       oklch(0.34 0.004 286)
--muted:      oklch(0.52 0.015 290)
--ocre:       oklch(0.68 0.12 66)     /* the live accent (highest chroma) */
--ocre-deep:  oklch(0.60 0.12 60)
--ocre-wash:  oklch(0.935 0.05 76)
```

> **Palette decision (confirmed).** The original brief mentioned "purples," but in the final materials **purple was deliberately removed** in favor of dark grey. Ochre is the single saturated accent. The `--purple` tokens are tuned to near-neutral grey (chroma ~0.004). This is intentional.

### Aesthetic
Terminal/"hacker" accents in JetBrains Mono (`>_ hands-on workshop ▋`). Clean, high-whitespace, one idea per slide, investor-ready. Tables for toolkit and timeline.

---

## 2. Session structure (timing)

| Segment | Min | Block | Format |
|---|---|---|---|
| 00:00–00:10 | 10 | **Outlearn** — "wow" demo, build a mini-app live in ~3 min | Demo |
| 00:10–00:30 | 20 | **Vibe coding 101** — theory blocks (see §3) | Lecture |
| 00:30–00:35 | 5 | **Setup check** — everyone with Claude + browser OK | Logistics |
| 00:35–01:00 | 25 | **Exercise A — Design** (Claude Design) | Hands-on |
| 01:00–01:40 | 40 | **Exercise B — Build** (Claude + Artifacts) | Hands-on |
| 01:40–01:50 | 10 | **Advanced demo** — Claude Code, Expo Go, Cowork | Demo |
| 01:50–02:00 | 10 | **Showcase + close + resources** | Plenary |

---

## 3. Theory content (as delivered in the deck)

### 3.1 Outlearn framing (slides 3-4) — Pascal Finette
Opening hook: speed of learning beats breadth of knowledge.
- **Slide 3** — "You can't out-know change. You can only outlearn it." Loop: Detect → Contain → Learn → Adapt. Attribution: Pascal Finette, *Outlearn* (rdcl.is/outlearn · finette.com).
- **Slide 4** — "Your speed of learning is inversely proportional to the cost of failure." Prototyping pushes failure cost → 0.

### 3.2 What is vibe coding? (slide 5)
Describe intent in plain language; AI writes the code; you steer/test/adjust instead of writing line by line.

### 3.3 Origin and evolution (slide 6)
- FEB 2025: Karpathy coins term on X.
- NOV 6 2025: Collins Word of the Year (+ Merriam-Webster).
- FEB 2026: "agentic engineering" (Karpathy, karpathy.ai).
- Framing: vibe coding = prototype/validate; agentic engineering = production with supervision.

### 3.4 Why it matters — JTBD framing (slide 7)
The job is to validate the idea, not to write code. Prototype stops being a bottleneck. Spreadsheet analogy.

### 3.5 The 4 Ds for directing AI (slide 8)
Delegation · Description · Discernment · Diligence. (Anthropic AI Fluency framework.)

### 3.6 The toolkit — "Where to start" (slide 9)
Table with 6 tools:

| Tool | What it does | When | Friction |
|---|---|---|---|
| Claude + Artifacts | Conversation + runnable web artifacts | Functional web prototype, zero install | Low |
| Claude Design | Design canvas: mockups + design systems | Designing the idea before building | Low |
| Claude Cowork | Agentic desktop app for non-devs | Setting up environment without terminal | Medium |
| VS Code / Cursor | AI-powered code editor | Building and versioning for real | Med-high |
| Claude Code | Terminal coding agent | Taking prototype to real app/site | High |
| Expo Go | Runs mobile prototypes on phone | Seeing app on real device instantly | High |

### 3.7 The spec-first method (slide 10)
A good prompt has five parts: Role/goal · Context · Constraints · Format · Iteration.

### 3.8 Four principles for better vibe coding (slide 11)
1. Think before building
2. Simplicity first
3. Surgical changes
4. Goal-driven execution

Attribution: andrej-karpathy-skills (community repo, MIT license — not authored by Karpathy himself).

### 3.9 Core idea (slide 12)
> "You can outsource your thinking, but you cannot outsource your understanding."

Attribution: k kache (@yacineMTB), Feb 3 2026 (x.com/yacineMTB/status/2018886083120153046). Later cited by Karpathy on Apr 30 2026. Traces to a François Fleuret thread.

### 3.10 Limits and risks (slide 13)
Hallucination · Security (no secrets in prompts) · Technical debt · When to escalate · Ownership & licensing.

### 3.11 Exercises briefing (slides 14-16)
Default case: **FreshBox** — weekly healthy meal-box for time-poor families.
- **Exercise A (Design, 25 min)**: brief → mockup → mini design system → iterate.
- **Exercise B (Build, 40 min)**: describe → generate Artifact → iterate 3-4 times → 60-sec pitch.

### 3.12 Advanced / optional track (slides 17-21)
Slides tagged `>_ optional · after the workshop`.
- Prototype → product maturity ladder (Validate → Build for real → Publish).
- Expo Go: how to run a mobile app on the phone.
- VS Code vs Cursor comparison.
- Resources grouped A-E (see §6).

---

## 4. Exercises (full detail)

### 4.1 Default case — FreshBox
Weekly healthy meal-box service for time-poor families. Urban couples and families aged 30-45. Value: balanced menus, optimized shopping list, zero waste. Used by anyone who doesn't bring their own idea.

### 4.2 Exercise A — Design (Claude Design, 25 min)
1. (5 min) Write the brief: product, audience, key sections.
2. (10 min) Ask for a mockup of main screen(s).
3. (5 min) Generate a mini design system: palette, typography, components.
4. (5 min) Iterate one screen.

**Deliverable:** 1-3 mockup screens + basic design system.
**Done when:** attendee can explain each design choice (discernment).

**Prompt template:**
```
You are a product designer. Create the mockup of the main screen of [PRODUCT],
a [web/app] for [AUDIENCE] that solves [PROBLEM]. Include [key sections].
Style: [adjectives]. Also generate a coherent color palette and typography.
No lorem ipsum — use realistic copy.
```

### 4.3 Exercise B — Build (Claude + Artifacts, 40 min)
1. (5 min) Describe the app, reusing the brief from Exercise A.
2. (15 min) Generate the Artifact and test it in the panel.
3. (15 min) Iterate 3-4 times: add section, change behavior, adjust styling.
4. (5 min) Prepare 60-second pitch.

**Deliverable:** functional Artifact (web app).
**Done when:** prototype does at least one interactive thing.

**Prompt template:**
```
Build a working web prototype of [PRODUCT] for [AUDIENCE]. It must have:
[screen 1], [screen 2], and [one concrete interaction — e.g. a booking form
or a calculator]. Apply this visual identity: [palette + typography from
Exercise A]. Make it a single file, responsive, with realistic copy.
```

---

## 5. Prompt templates (all four, exact as printed)

**A · Design:**
> You are a product designer. Create the mockup of the main screen of [PRODUCT], a [web/app] for [AUDIENCE] that solves [PROBLEM]. Include [key sections]. Style: [adjectives]. Also generate a coherent color palette and typography. No lorem ipsum — use realistic copy.

**B · Build:**
> Build a working web prototype of [PRODUCT] for [AUDIENCE]. It must have: [screen 1], [screen 2], and [one concrete interaction — e.g. a booking form or a calculator]. Apply this visual identity: [palette + typography from Exercise A]. Make it a single file, responsive, with realistic copy.

**↻ Iterate:**
> Now [change X / add Y / simplify Z]. Keep everything else the same, and show me only what changed.

**! Debug / fix:**
> This isn't working: [what happens], but I expected [what you wanted]. Relevant part: [paste code / screenshot]. Find the cause, fix it, and tell me in one line what was wrong.

---

## 6. Resources (as printed in deck and handout)

### A. Understand and direct AI
- Anthropic Academy — AI Fluency: Framework & Foundations: anthropic.skilljar.com/ai-fluency-framework-foundations
- Anthropic Academy — Claude 101: anthropic.com/learn

### B. Mobile app (Expo)
- Expo tutorial "StickerSmash": docs.expo.dev/tutorial
- Get started / create-expo-app: docs.expo.dev/get-started
- Expo Snack (online playground): snack.expo.dev
- Expo Go app: App Store / Google Play

### C. AI editor (IDE)
- VS Code Get started: code.visualstudio.com
- vscode.dev (no install)
- Cursor: cursor.com
- Claude Code: docs.claude.com (Claude Code section)

### D. Publish / deploy
- Cloudflare Pages: pages.cloudflare.com
- Vercel: vercel.com (Hobby = no commercial use)
- GitHub Pages: pages.github.com
- GitHub: github.com

### E. Automate setup
- Anthropic Academy — Claude Cowork: anthropic.com/learn

### Recommended path
1. Understand: AI Fluency (Anthropic Academy)
2. Tool: Claude 101 + Claude Code in Action
3. Mobile: Expo "StickerSmash" tutorial
4. Editor: VS Code Get started (or Cursor)
5. Publish: Cloudflare Pages + GitHub

---

## 7. Session prerequisites (as published on the GitHub Pages site)

Sent to students 3-5 days before the session:

| # | Type | Item |
|---|---|---|
| 1 | Required | Claude account with active Pro subscription (claude.ai) |
| 2 | Required | GitHub account + basic familiarity. Links: github.com/signup · Introduction to GitHub (youtube.com/watch?v=r8jQ9hVA2qs) · Know more: GitHub 101 playlist |
| 3 | Required | One idea to prototype (if none, FreshBox is provided) |
| 4 | Recommended | Claude desktop app installed (support.claude.com/es/articles/10065433-instalar-claude-desktop) |
| 5 | Recommended | Claude extension for Google Chrome (claude.com/claude-for-chrome) |

---

## 8. Verified external references

All claims and quotes confirmed accurate as of June 2026:

- [x] **Collins "Word of the Year 2025" — Nov 6 2025** (slide 6). Confirmed: Collins Dictionary blog, CNN, Mashable.
- [x] **Karpathy "From Vibe Coding to Agentic Engineering"** + karpathy.ai (slide 6). Author-confirmed.
- [x] **Pascal Finette — "Outlearn"** quotes + URLs rdcl.is/outlearn and finette.com (slides 3-4). Author-confirmed.
- [x] **@yacineMTB quote** (slide 12). Confirmed: posted Feb 3 2026, 9:15 PM, tweet 2018886083120153046; wording matches exactly. Traces to a François Fleuret thread; Karpathy cited it on Apr 30 2026.
- [x] **andrej-karpathy-skills (MIT)** — community repo distilling Karpathy's observations; NOT authored by Karpathy.
- [x] **Cursor / Vercel free-plan caveats** — verified.
- [x] **Resource URLs** — author-confirmed; re-check the day before, as platforms change.

---

## 9. Open items / placeholders

- `[GITHUB REPO LINK]` — appears on deck slide 22 and handout pages 2 and 3. The repo URL is https://github.com/carlos-spitzer/intro-to-vibe-coding. QR codes to be generated and inserted before printing.

---

## 10. How the materials were created (process record)

1. **Planning SPEC** (this file, original version) — defined objectives, audience, timing, exercises, visual identity.
2. **Main Claude Design prompt** (`prompt-claude-design.md`) — generated deck + handout + cheat sheet in one session.
3. **Iterative additions in Claude Design** (captured in the same prompt file):
   - Pascal Finette Outlearn opener (slides 3-4): introduced directly in Claude Design, not in the original prompt.
   - Karpathy four principles (slide 11): added via a focused sub-prompt.
   - @yacineMTB core-idea quote (slide 12): introduced in Claude Design.
   - "If you want to do more" section (slides 17-21 + handout p3): added with the resource list sub-prompt.
4. **GitHub Pages landing site** (`index.html`) — built separately in Claude Code, not generated by Claude Design.

> To recreate from scratch: attach this SPEC to Claude Design, run `prompt-claude-design.md` in a single session, then manually re-add the Outlearn opener, @yacineMTB quote, and Karpathy principles if not already present from the prompt.

---

## 11. Divergences from original planning

- Deck grew from ~14 to **22 slides**.
- **Outlearn framing** (Pascal Finette, slides 3-4) added as session opener.
- **@yacineMTB quote** (slide 12) added as the session's core idea.
- **Toolkit table** expanded: VS Code/Cursor added as a sixth tool.
- **Palette**: purple removed in favor of dark grey; ochre is the sole accent.
- **Four principles slide** (slide 11): added from andrej-karpathy-skills.
- **GitHub Pages site**: not in the original plan; built to host all materials publicly.
