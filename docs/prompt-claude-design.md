# Prompt for Claude Design — Workshop "Intro to Vibe Coding"

> **How to use this file.**
> 1. Open a new Claude Design session.
> 2. Attach (or paste in full) `workshop-vibecoding-SPEC.md` — it is the source of truth for all content.
> 3. Copy the prompt block below and paste it into Claude Design.
> 4. Work deliverable by deliverable in the order indicated; validate before moving to the next.
>
> This single prompt file replaces the original two-file approach (main prompt + siguiente-paso addendum). Everything is consolidated here.

---

## Prompt block (copy from here)

```
ROLE AND OBJECTIVE
You are an instructional and presentation designer. Your objective is to generate the complete visual materials for a 120-minute hands-on workshop titled "Vibe coding — from idea to prototype in a single session," aimed at NON-technical students in an Exec. Master in Digital Business, Innovation and Entrepreneurship (EMBDIE).

SOURCE OF TRUTH
Use the SPEC document I have attached as the only source of content and structure. Do not invent data, figures, tools, quotes, or product capabilities that are not in the SPEC. If you need a fact that is not there, leave it as a [VERIFY] placeholder.

LANGUAGE AND TONE
All text in English. Conversational but professional tone, direct, no motivational filler or opener phrases like "Great!" or "Absolutely!". No em-dash (—): replace with a comma or semicolon depending on context.

VISUAL IDENTITY (mandatory — apply consistently across all deliverables)
Typography:
- Display / headings: Space Grotesk
- Body / UI text: Hanken Grotesk
- Code / prompts / terminal accents: JetBrains Mono

Palette (OKLCH values — use these exactly):
- --ink:       oklch(0.22 0.02 292)   /* near-black */
- --paper:     oklch(0.975 0.006 85)  /* warm off-white */
- --grey:      oklch(0.34 0.004 286)
- --muted:     oklch(0.52 0.015 290)
- --ocre:      oklch(0.68 0.12 66)    /* primary accent */
- --ocre-deep: oklch(0.60 0.12 60)
- --ocre-wash: oklch(0.935 0.05 76)
NOTE: no purple. Ochre is the single saturated accent; everything else is near-neutral.

Aesthetic: clean, high-whitespace, one idea per slide, investor-ready. Terminal-style accents in JetBrains Mono (e.g. ">_ hands-on workshop ▋", ">_ optional · after the workshop"). Tables for the toolkit and timeline — legible from 3 metres away.

Footer on every slide/page: "> Vibe coding · EMBDIE · June 2026" plus a page/slide number.

---

DELIVERABLE 1 — THEORY DECK (22 slides)

Generate exactly 22 slides in this order. The content for each is in the SPEC; this list is the structural skeleton:

01 · Cover: title "Vibe coding" + subtitle "From idea to prototype in a single session" + author Carlos Spitzer + EMBDIE + ">_ hands-on workshop ▋"
02 · Session map: "Four moments, two hours" — 10' Outlearn · 20' Vibe coding 101 · 65' Practice · 15' Showcase
03 · Outlearn: "You can't out-know change. You can only outlearn it." — Pascal Finette's Detect→Contain→Learn→Adapt loop
04 · Fail cheap, learn fast: "Your speed of learning is inversely proportional to the cost of failure." — Pascal Finette, Outlearn
05 · What is vibe coding? One-sentence definition
06 · Origin and evolution: Karpathy Feb 2025 → Collins Word of the Year Nov 6 2025 → "agentic engineering" Feb 2026
07 · Why it matters: JTBD framing — the job is to validate the idea, not write code
08 · The 4 Ds: Delegation · Description · Discernment · Diligence (visual grid)
09 · The toolkit: "Where to start…" — table with 6 tools (see SPEC §3.6 and toolkit table)
10 · The spec-first method: "A good prompt has five parts" — Role/goal · Context · Constraints · Format · Iteration
11 · Four principles: Think before building · Simplicity first · Surgical changes · Goal-driven execution. Credit: andrej-karpathy-skills (MIT)
12 · Core idea: "You can outsource your thinking, but you cannot outsource your understanding." — @yacineMTB (k kache), Feb 3 2026
13 · Limits and risks: Hallucination · Security · Technical debt · When to escalate · Ownership & licensing
14 · Practice intro: "Two exercises, your own idea" — 25' Exercise A (Design) + 40' Exercise B (Build). Default case: FreshBox
15 · Exercise A briefing: Design the idea (Claude Design, 25 min) — 4 steps, deliverable, "done" criterion, prompt template reference
16 · Exercise B briefing: Build the prototype (Claude + Artifacts, 40 min) — 4 steps, deliverable, "done" criterion, prompt template reference
17 · If you want more intro: ">_ optional · after the workshop" — overview of the advanced track
18 · Prototype to product: 3-step maturity ladder — Validate (Artifacts+Design) → Build for real (IDE+Claude Code) → Publish (Expo Go / Cloudflare Pages / Vercel)
19 · Expo Go: your app on a real phone — 3-step diagram: write/generate → dev server shows QR → scan with Expo Go
20 · The editor with superpowers: VS Code (free/OSS, vscode.dev, AI agent mode) vs Cursor (AI-first, Composer, free+paid)
21 · Resources: grouped A-E from the SPEC + Recommended path (5 steps) + [QR / GITHUB REPO LINK] placeholder
22 · Close: "What you walk away with" — Today / Advanced track / Remember (prototype ≠ production; never paste secrets; escalate in time). Bottom: ">_ All materials in this GitHub repo: [GITHUB REPO LINK]"

Deck requirements: short affirmative titles; at most 6 lines of text per slide; use simple iconography and diagrams instead of paragraphs; tables (toolkit, timeline) must be legible from 3 metres.

Pause after the deck for review before continuing with Deliverable 2.

---

DELIVERABLE 2 — STUDENT HANDOUT (3 pages, print-ready worksheet)

Header on every page: "Vibe coding · Worksheet" / "Exec. Master · Workshop handout"
Footer: standard ("> Vibe coding · EMBDIE · June 2026 · N / 3")

Page 1 — Exercise A:
- Intro paragraph: turn your idea into a mockup and a working prototype, no code needed.
- Default case FreshBox (1 short paragraph from the SPEC).
- Exercise A "Design the idea" (Claude Design, 25 min): goal, 4 checkbox steps with time allocations (5/10/5/5 min), a blank "your brief" writing area, and the Design prompt template (from the SPEC) with fillable [brackets].

Page 2 — Exercise B:
- Exercise B "Build the prototype" (Claude + Artifacts, 40 min): goal, 4 checkbox steps (5/15/15/5 min), a blank "notes" writing area, and the Build prompt template with fillable [brackets].
- "3 key risks to keep in mind": Hallucination · Security · Technical debt (1 line each).
- QR/link box: [GITHUB REPO LINK] placeholder.

Page 3 — If you want to do more:
- Resources grouped A-E (from SPEC §6).
- Recommended path (5 steps).
- "Two honesty notes": Cursor and Vercel free-plan limits; verify links/plans the day before.
- QR/link box: [GITHUB REPO LINK] placeholder.

Style: plenty of writing space, checklist-style checkboxes, same visual identity as the deck. No lorem ipsum.

Pause after the handout for review before continuing with Deliverable 3.

---

DELIVERABLE 3 — PROMPT CHEAT SHEET (1 page, quick reference)

Header: "Prompt · Cheat Sheet" / "Exec. Master · Quick reference"
Footer: standard.

Section 1 — The spec-first method (5 parts, visual and compact):
Role/goal · Context · Constraints · Format · Iteration

Section 2 — Copy-paste templates (fill the [brackets]), all four:
- A Design (Claude Design)
- B Build (Claude + Artifacts)
- Iterate
- Debug / fix
(Use exact wording from SPEC §5.)

Section 3 — Do's & Don'ts (5 items):
- Give role, context, constraints and format in every prompt.
- Iterate in small steps, one change at a time.
- Read the output critically before you trust it.
- Never paste credentials, personal data, or secrets.
- Don't ship a prototype as production; escalate for real data, payments, or maintenance.

Dense but legible, single page, same palette.

---

OUTPUT FORMAT AND ITERATION INSTRUCTIONS
- Deliver the 3 materials as separate, editable HTML artifacts.
- Start with Deliverable 1 (deck). After generating it, list in 3 bullets the design decisions made and the content points that need review before printing.
- Only continue to Deliverable 2 after explicit approval.
- After each deliverable, call out any [VERIFY] or [bracket] placeholders that remain.
- Do not use lorem ipsum anywhere: all copy must be realistic English based on the SPEC.
```

---

## Usage notes (do not copy into Claude Design)

### Order of work
1. Attach `workshop-vibecoding-SPEC.md` to the session first.
2. Paste the prompt block above.
3. Review and approve the deck before requesting the handout.
4. Review and approve the handout before requesting the cheat sheet.
5. After all three are approved, export as HTML for printing and hosting.

### Items to verify before each session
- Current Claude plan limits (Free/Pro/Team): support.claude.com
- Claude Design and Artifacts capabilities: docs.claude.com
- Expo Go features: docs.expo.dev
- Cursor pricing/plans: docs.cursor.com
- Vercel Hobby plan terms: vercel.com/pricing
- All resource URLs in SPEC §6: platforms change.

### Placeholders to fill before printing
- `[GITHUB REPO LINK]` appears on deck slide 22 and handout pages 2 and 3. Current URL: https://github.com/carlos-spitzer/intro-to-vibe-coding. Generate a QR code from this URL and insert it into the placeholder boxes.

### What is NOT in this prompt
The **GitHub Pages landing site** (`index.html`) was built separately in Claude Code, not generated by Claude Design. It is part of the repository but does not need to be recreated through this prompt.

### Honesty notes (keep in the materials)
- Cursor: limited free plan + paid plans. Do not present it as fully free.
- Vercel Hobby: no commercial use. State this explicitly.
- andrej-karpathy-skills: MIT-licensed community repo, not authored by Karpathy himself.
- Vibe coding is for prototyping and validation, not for production without oversight.

### How to show students the creation process
To demonstrate how these materials were built from scratch, the narrative is:
1. Define the workshop objectives and audience → produces this SPEC.
2. Translate the SPEC into a structured design prompt → this file.
3. Paste into Claude Design → generates the three visual materials.
4. Iterate with focused sub-prompts for additions (Outlearn opener, Karpathy principles, @yacineMTB quote).
5. Build the GitHub Pages site using Claude Code with this SPEC as context.
This is itself an example of vibe coding applied to instructional design.
