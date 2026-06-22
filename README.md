# Intro to Vibe Coding

> A 2-hour, hands-on workshop that takes non-engineers from idea to working prototype in a single session.

**Author:** Carlos Spitzer
**Program:** Exec. Master, Digital Business, Innovation & Entrepreneurship (EMBDIE)
**Date:** June 2026 · **Language:** English

This repository holds all the materials for the workshop. Everything is plain HTML you can open in a browser or print:

| File | What it is |
|---|---|
| [`index.html`](index.html) | Landing page that links the three materials |
| [`Vibe Coding Workshop - Deck.html`](Vibe%20Coding%20Workshop%20-%20Deck.html) | The 23-slide theory deck |
| [`Vibe Coding Workshop - Cheat Sheet.html`](Vibe%20Coding%20Workshop%20-%20Cheat%20Sheet.html) | One-page prompt quick reference |
| [`Vibe Coding Workshop - Student Handout.html`](Vibe%20Coding%20Workshop%20-%20Student%20Handout.html) | Three-page student worksheet |
| [`docs/workshop-vibecoding-SPEC.md`](docs/workshop-vibecoding-SPEC.md) | As-built specification, the single source of truth for recreating or editing the set |
| [`docs/prompt-claude-design.md`](docs/prompt-claude-design.md) | The Claude Design prompt that generated the materials, so the whole set can be rebuilt from scratch |

---

## Why these materials exist

The premise of the workshop is simple: **your job isn't to write code, it's to validate the idea.** For founders, product people, and executives, the prototype has historically been the bottleneck, the thing you had to wait on engineering for before you could test whether an idea was worth pursuing at all.

Vibe coding removes that bottleneck. You describe intent in plain language, the AI writes the code, and you steer, test, and adjust instead of writing line by line. That turns "weeks to a prototype" into "a single session," which changes *what kinds of ideas are worth trying at all.*

The deeper rationale comes from two ideas that frame the whole session:

- **You can't out-know change, you can only outlearn it.** Speed-to-learn beats speed-to-know. The faster and cheaper you can fail, the faster you adapt. Prototyping pushes the cost of failure toward zero, which is exactly what makes fast learning possible.
- **You can outsource your thinking, but you cannot outsource your understanding.** Vibe coding is leverage, not a replacement for judgment. It works as long as you stay the person who understands what is being built and why.

The materials exist to give a non-technical audience an honest, practical on-ramp: enough method to be productive in one sitting, and enough about the limits (hallucination, security, technical debt, when to escalate) to know that a prototype is not a production system.

---

## Credits and attribution

These materials stand on the work of others. Credit where it's due:

- **Pascal Finette** for "Outlearn" and "fail cheap, learn fast" (rdcl.is/outlearn · finette.com), which open the workshop.
- **Andrej Karpathy**, who coined the term *vibe coding* (Feb 2025) and authored "From Vibe Coding to Agentic Engineering" (karpathy.ai). The framing of vibe coding (prototype/validate) versus agentic engineering (production with supervision) follows his distinction.
- **k kache (@yacineMTB)** for the line "you can outsource your thinking, but you cannot outsource your understanding" (3 Feb 2026); it traces to a François Fleuret thread that Yacine amplified, and was later cited by Karpathy.
- **andrej-karpathy-skills** (community repo, MIT license), which distills Karpathy's observations into the four principles for better vibe coding. Community-authored, *not* by Karpathy himself.
- **Anthropic** for the AI Fluency framework (the 4 Ds: Delegation, Description, Discernment, Diligence) and the Claude tooling (Claude + Artifacts, Claude Design, Claude Cowork, Claude Code) the exercises are built around.

All external claims and quotes in the materials were verified accurate as of June 2026; see §8 of the [SPEC](docs/workshop-vibecoding-SPEC.md) for the full verification checklist.

---

## Fundamentals the workshop teaches

The method distilled to its core:

1. **Spec-first prompting.** A good prompt has five parts: Role/goal · Context · Constraints · Format · Iteration.
2. **The 4 Ds for directing AI.** Delegation (what to ask) · Description (how to ask) · Discernment (is it right?) · Diligence (own the outcome).
3. **Four principles.** Think before building · Simplicity first · Surgical changes · Goal-driven execution.
4. **Know the limits.** Hallucination, security (never paste secrets), technical debt, and knowing when to escalate from prototype to production.

The hands-on portion runs two exercises on a default case (**FreshBox**): *Design the idea* (Claude Design) and *Build the prototype* (Claude + Artifacts).

---

## How to use this repo

Open [`index.html`](index.html) in any browser, or open the deck, cheat sheet, and handout directly. They are self-contained, print-friendly, and need no build step or dependencies.

## License and reuse

Workshop content © Carlos Spitzer, 2026. The third-party ideas above belong to their respective authors and are used with attribution. The andrej-karpathy-skills guidelines are MIT-licensed by their community authors.
