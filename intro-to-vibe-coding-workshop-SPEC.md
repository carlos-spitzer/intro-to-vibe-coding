# SPEC (AS-BUILT) — Vibe Coding Workshop Materials

> **Purpose of this document.** This is a faithful, as-built specification of the three materials actually produced in Claude Design: the **Theory Deck**, the **Prompt Cheat Sheet**, and the **Student Handout**. It documents the final state so the set can be recreated or re-edited later. It replaces the earlier planning SPEC (which described intent; this describes the delivered result).
>
> **Status:** delivered HTML, June 2026. Placeholders still open: see §8.

---

## 0. Meta / identity

| Field | As-built value |
|---|---|
| Title | **Vibe coding** — "From idea to prototype in a single session" |
| Author / byline | Carlos Spitzer |
| Program | Exec. Master · Digital Business, Innovation & Entrepreneurship (**EMBDIE**) |
| Date stamp | June 2026 |
| Language | English |
| Deliverables | (1) Theory Deck — 22 slides · (2) Prompt Cheat Sheet — 1 page · (3) Student Handout — 3 pages |
| Per-page footer | `> Vibe coding · EMBDIE · June 2026` + page/slide number (deck: `NN / 22`; handout: `N / 3`) |

---

## 1. Design system (as-built)

Extracted from the deck's CSS — use these exact tokens to recreate the look.

### Typography
| Role | Font |
|---|---|
| Display / headings | **Space Grotesk** |
| Body / UI | **Hanken Grotesk** |
| Code / prompts / terminal accents | **JetBrains Mono** |

### Color tokens (defined in OKLCH, not hex)
Named CSS variables: `--ink`, `--ink-2`, `--paper`, `--paper-2`, `--white`, `--line`, `--line-soft`, `--grey`, `--grey-bright`, `--grey-wash`, `--muted`, `--purple`, `--purple-bright`, `--purple-wash`, `--ocre`, `--ocre-deep`, `--ocre-wash`.

Reference values:
```
--ink:        oklch(0.22 0.02 292)    /* near-black, slight violet */
--paper:      oklch(0.975 0.006 85)   /* warm off-white background */
--white:      oklch(0.995 0.003 85)
--grey:       oklch(0.34 0.004 286)
--muted:      oklch(0.52 0.015 290)
--ocre:       oklch(0.68 0.12 66)     /* the live accent (highest chroma) */
--ocre-deep:  oklch(0.60 0.12 60)
--ocre-wash:  oklch(0.935 0.05 76)
--purple:     oklch(0.34 0.004 286)   /* NOTE: tuned to near-neutral grey */
```
Layout padding tokens: `--pad-x: 116px`, `--pad-y: 84px`.

> **Palette decision (confirmed).** The original brief mentioned "black, grey, white, purples, ochre," but in the final deck **purple was deliberately removed in favor of dark grey** — the `--purple` tokens are intentionally tuned to near-neutral grey (chroma ~0.004), and **ochre is the single saturated accent** (chroma ~0.12). This is the intended look, not drift. If you ever want to reintroduce purple, raise the chroma on the `--purple*` tokens (e.g. `oklch(0.45 0.10 300)`).

### Aesthetic
Terminal/"hacker" accents in JetBrains Mono (`>_ hands-on workshop ▋`, `>_ optional · after the workshop`, prompt blocks rendered as code). Clean, high-whitespace, one idea per slide, investor-ready. Tables used for the toolkit and timeline.

---

## 2. Document 1 — Theory Deck (22 slides)

Slide-by-slide as built. Header label = the small section tag shown top-left.

| # | Section label | Slide title | Key content |
|---|---|---|---|
| 01 | (cover) | **Vibe coding** | Subtitle "From idea to prototype in a single session"; author Carlos Spitzer; EMBDIE byline; `>_ hands-on workshop ▋`. |
| 02 | Session map | **Four moments, two hours** | 10' **Outlearn** (why speed to learn wins + 3-min live build) · 20' **Vibe coding 101** · 65' **Practice** · 15' **Showcase**. |
| 03 | Outlearn · why this matters | **You can't out-know change. You can only outlearn it.** | Loop: Detect → Contain → Learn → Adapt ↺. Vibe coding shrinks the loop from months to minutes. Attribution: Pascal Finette · "Outlearn" (rdcl.is/outlearn · finette.com). |
| 04 | Outlearn · fail cheap, learn fast | **Fail cheap, learn fast.** | "The speed of learning is inversely proportional to the cost of failure" (Pascal Finette). Prototyping pushes failure cost → 0. |
| 05 | Vibe coding 101 · what is it | **What is vibe coding?** | Describe intent in plain language; AI writes the code; you steer/test/adjust instead of writing line by line. |
| 06 | Vibe coding 101 · origin & evolution | **From a tweet to a discipline** | Timeline: FEB 2025 Karpathy coins term · NOV 6 2025 Collins Word of the Year (+ Merriam-Webster) · FEB 2026 "agentic engineering". Contrast: vibe coding = prototype/validate vs agentic engineering = production w/ supervision. Link: "From Vibe Coding to Agentic Engineering" (karpathy.ai). |
| 07 | Vibe coding 101 · why it matters | **Your job isn't to write code. It's to validate the idea.** | JTBD framing; prototype stops being a bottleneck; spreadsheet analogy. |
| 08 | Vibe coding 101 · AI fluency | **The 4 Ds for directing an AI** | Delegation (what to ask) · Description (how to ask) · Discernment (is it right?) · Diligence (own the outcome). |
| 09 | Vibe coding 101 · the toolkit | **Where to start…** | Table — Tool / What it does / When / Friction: Claude+Artifacts (Low) · Claude Design (Low) · Claude Cowork (Medium) · VS Code/Cursor (Med-high) · Claude Code (High) · Expo Go (High). Pointer to slides 17–19. |
| 10 | Vibe coding 101 · spec-first method | **A good prompt has five parts** | Role/goal · Context · Constraints · Format · Iteration. Example prompt (monospace). |
| 11 | Vibe coding 101 · four principles | **Four principles for better vibe coding** | Think before building (fixes silent assumptions) · Simplicity first (bloat) · Surgical changes (unwanted edits) · Goal-driven execution (vague loops). Punchline + "andrej-karpathy-skills guidelines (MIT)". |
| 12 | Vibe coding 101 · the core idea | **"You can outsource your thinking, but you cannot outsource your understanding."** | Attributed: k kache · @yacineMTB · Feb 3 2026 (x.com link). Tag: describing well > knowing how to code — if you stay the one who understands. |
| 13 | Vibe coding 101 · limits & risks | **Know where it falls short** | Hallucination · Security (no secrets in prompts) · Technical debt · When to escalate · Ownership & licensing. |
| 14 | Practice · now it's your turn | **Two exercises, your own idea** | 25' A Design (Claude Design) · 40' B Build (Claude + Artifacts). Default case: **FreshBox**. |
| 15 | Practice · exercise A · design | **Design the idea** | Objective; 4 guided steps (5/10/5/5'); deliverable (1–3 mockup screens + design system); "done" = can explain each choice (discernment); template ref. |
| 16 | Practice · exercise B · build | **Build the prototype** | Objective; 4 guided steps (5/15/15/5'); deliverable (working Artifact); "done" = ≥1 interactive thing; template ref. |
| 17 | If you want more | **If you want to go deep…** | `>_ optional · after the workshop`. Prototype → product; Expo Go; VS Code/Cursor; Resources. |
| 18 | If you want more · the next step | **From prototype to product** | 1 Validate (Artifacts + Design) → 2 Build for real (IDE + Claude Code) → 3 Publish (Expo Go and/or Cloudflare Pages/Vercel). "Know when to ask for technical help." |
| 19 | If you want more · mobile | **Your app on a real phone: Expo Go** | 3 steps (write/generate code → dev server shows QR → scan with Expo Go). One codebase iOS/Android/web. Honest note: needs Node.js + terminal. |
| 20 | If you want more · the editor | **The editor with superpowers** | VS Code (free/OSS, vscode.dev, AI agent mode) vs Cursor (AI-first on VS Code, Composer, free + paid). Both pair with Claude Code. |
| 21 | If you want more · resources | **Resources to take the next step** | Grouped A–E (see §6) + Recommended path (5 steps). |
| 22 | Closing | **What you walk away with** | Today / Advanced track / Remember (prototyping ≠ production; never paste secrets; escalate in time). `>_ All materials … in this GitHub repo: [GITHUB REPO LINK]`. |

---

## 3. Document 2 — Prompt Cheat Sheet (1 page)

Header: "Prompt · Cheat Sheet" · "Exec. Master · Quick reference". Footer: standard.

**Section 1 — The spec-first method (5 parts):** Role/goal · Context · Constraints · Format · Iteration.

**Section 2 — Copy-paste templates (fill the [brackets]):** four templates — A Design, B Build, ↻ Iterate, ! Debug/fix. Exact wording in §6.

**Section 3 — Do's & Don'ts:**
- ✓ Give role, context, constraints & format in every prompt.
- ✓ Iterate in small steps — one change at a time.
- ✓ Read the output critically before you trust it.
- ✗ Never paste credentials, personal data, or secrets.
- ✗ Don't ship a prototype as production — escalate for real data, payments, or maintenance.

---

## 4. Document 3 — Student Handout (3 pages)

Header: "Vibe coding · Worksheet" · "Exec. Master · Workshop handout".

**Page 1/3 — Exercise A.** Intro (turn an idea into a mockup + a working prototype, no code) + FreshBox default case. Exercise A "Design the idea" (Claude Design, 25 min): goal, 4 checkbox steps (5/10/5/5'), a blank "your brief" area, and the **design prompt template** (§6).

**Page 2/3 — Exercise B.** "Build the prototype" (Claude + Artifacts, 40 min): goal, 4 checkbox steps (5/15/15/5'), a blank "notes" area, and the **build prompt template** (§6). Then "Keep in mind — 3 key risks": Hallucination · Security · Technical debt. QR/link box → `[GITHUB REPO LINK]`.

**Page 3/3 — If you want to do more.** Resources grouped A–E (§6) + Recommended path + "Two honesty notes" (Cursor/Vercel free-plan limits; verify links/plans the day before). QR/link box → `[GITHUB REPO LINK]`.

---

## 5. (reserved)

---

## 6. Reusable prompt templates & resource list (exact as-built text)

### Prompt templates
**A · Design (Claude Design):**
> You are a product designer. Create the mockup of the main screen of [PRODUCT], a [web/app] for [AUDIENCE] that solves [PROBLEM]. Include [key sections]. Style: [adjectives]. Also generate a coherent color palette and typography. No lorem ipsum — use realistic copy.

**B · Build (Claude + Artifacts):**
> Build a working web prototype of [PRODUCT] for [AUDIENCE]. It must have: [screen 1], [screen 2], and [one concrete interaction — e.g. a booking form or a calculator]. Apply this visual identity: [palette + typography from Exercise A]. Make it a single file, responsive, with realistic copy.

**↻ Iterate:**
> Now [change X / add Y / simplify Z]. Keep everything else the same, and show me only what changed.

**! Debug / fix:**
> This isn't working: [what happens], but I expected [what you wanted]. Relevant part: [paste code / screenshot]. Find the cause, fix it, and tell me in one line what was wrong.

### Resource list (grouped, as printed)
- **A · Understand & direct AI** — AI Fluency: Framework & Foundations (anthropic.skilljar.com) · Claude 101 (anthropic.com/learn).
- **B · Mobile app (Expo)** — Expo tutorial "StickerSmash" (docs.expo.dev/tutorial) · Get started / create-expo-app (docs.expo.dev/get-started) · Expo Snack (snack.expo.dev) · Expo Go app (App Store / Google Play).
- **C · AI editor (IDE)** — VS Code Get started (code.visualstudio.com) · vscode.dev · Cursor (cursor.com) · Claude Code (docs.claude.com/.../claude-code).
- **D · Publish / deploy** — Cloudflare Pages (pages.cloudflare.com) · Vercel (vercel.com; Hobby = no commercial) · GitHub Pages (pages.github.com) · GitHub (github.com).
- **E · Automate setup** — Claude Cowork (anthropic.com/learn).
- **Recommended path:** Understand → Tool → Mobile → Editor → Publish.

---

## 7. External references used — verification checklist

All claims/quotes in the materials are **verified accurate** — author-confirmed, with the two highest-risk items independently re-confirmed via web search (3 Jun 2026):

- [x] **Collins "Word of the Year 2025" — Nov 6 2025** (slide 6). Independently confirmed (Collins Dictionary blog, CNN, Mashable). Term coined by Karpathy, Feb 2025.
- [x] **Karpathy "From Vibe Coding to Agentic Engineering"** + `karpathy.ai` (slide 6). Author-confirmed.
- [x] **Pascal Finette — "Outlearn"** quotes + URLs `rdcl.is/outlearn`, `finette.com` (slides 3–4). Author-confirmed.
- [x] **@yacineMTB quote** (slide 12). Independently confirmed: posted by @yacineMTB (kache) 9:15 PM, 3 Feb 2026, tweet `2018886083120153046`; wording matches exactly. (Karpathy later cited the same line on 30 Apr 2026; it traces to a François Fleuret thread that Yacine amplified.)
- [x] **andrej-karpathy-skills (MIT)** — community repo distilling Karpathy's observations; *not* authored by Karpathy.
- [x] **Cursor / Vercel free-plan caveats.**
- [x] **Resource URLs** in §6 — author-confirmed; still worth a live re-check the day before, as platforms change.

---

## 8. Placeholders to fill before printing
- `[GITHUB REPO LINK]` — appears on deck slide 22 and handout pages 2 & 3 (+ QR). Add the repo URL and generate the QR.

---

## 9. How this set was created (process record)
1. **Planning SPEC** → defined objectives, audience, timeline, exercises, visual identity.
2. **Main Claude Design prompt** (`prompt-claude-design.md`) → generated deck + handout + cheat sheet (M1–M3).
3. **Addendum prompt** (`prompt-claude-design-siguiente-paso.md`) → added the "If you want to do more" section (deck slides 17–21 + handout p3) and the curated resource list.
4. **Karpathy slide prompt** (`prompt-claude-design-karpathy-slide.md`) → added deck slide 11 (four principles).
5. Manual additions during design: the **Outlearn** opener (Pascal Finette, slides 2–4) and the **core-idea** quote (slide 12) were introduced in Claude Design and are *not* in the original prompts — record them here so they aren't lost on a rebuild.

> To recreate from scratch: run prompts 2 → 3 → 4 in one Claude Design session with this SPEC attached, then re-add the items from step 5.

---

## 10. Divergences from the original plan (for the record)
- Deck grew from ~14 to **22 slides**.
- **New framing added**: Pascal Finette "Outlearn" (slides 3–4) as the opening hook.
- **New quote added**: @yacineMTB on outsourcing thinking vs understanding (slide 12).
- **Toolkit table** now includes **VS Code / Cursor** as a row (6 tools).
- **Palette**: purple deliberately removed in favor of dark grey; ochre is the sole accent (see §1 — intentional decision, confirmed).
