# FinLYNK — Decode the Finance Word Problem

A gamified, self-paced study companion for **MBA-level corporate finance**. Built for the one thing that trips students up most: **figuring out what to plug into which formula when reading a word problem.**

Same engine model as [chartlynk](https://github.com/allisonrowell/chartlynk) — a single self-contained `index.html`, no build step, no backend, progress saved in the browser (localStorage), XP + streak + progress bars.

> **Study tool.** Practice the method until picking the right formula becomes automatic — then do the real work yourself.

## The signature mechanic — the 5-stage Decoder

Every problem is worked as a game with five stages, earning XP at each:

1. **Read** — the word problem, numbers highlighted.
2. **Tag** — assign each number its role (PV, FV, r, t, C, g). *This is the core skill.*
3. **Formula** — pick the right formula from a shortlist; wrong picks explain *why* they're wrong.
4. **Plug in** — drop each tagged value into the formula's slots (with unit-conversion prompts).
5. **Solve** — the arithmetic reveals step by step, ending in the answer + a plain-English "what this means."

## Curriculum

Six tracks covering a full MBA corporate-finance course, each with lessons, quizzes, decoders, and an endless generated Drill Sandbox:
1. Time Value of Money
2. Capital Budgeting — NPV & IRR
3. Interest Rates & Bond Pricing
4. Stock Valuation / DDM
5. Risk, Return & Cost of Capital — WACC
6. Integrative — Valuation, EVA & MVA

## Run locally

```bash
open index.html
```

## Deploy

**Netlify Drop** (fastest): drag this folder onto https://app.netlify.com/drop → instant live URL.

**GitHub Pages:** push to a repo, then Settings → Pages → Deploy from branch → `main` / root.

## Editing content

All content lives in the `TRACKS` array near the top of the `<script>` in `index.html`. Each track has `steps`, and a step is one of `lesson`, `quiz`, or `decode`. To add a decoder, append a `decode` object: `scenario`, `ask`, `roles`, `givens` (with correct `role`), `formulas` (one `correct`), `plug` (template + `blanks` with accepted values), `solve` (steps), `answer`, and `meaning`.

---

FinLYNK is an independent study aid for MBA corporate finance, not affiliated with any university or course.
