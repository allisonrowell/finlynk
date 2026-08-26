# FinLYNK — Decode the Finance Word Problem

A gamified, self-paced study companion for **IMBA 6071 Financial Management** (Georgia Tech / Scheller, Prof. Clarke). Built for the one thing that trips students up most: **figuring out what to plug into which formula when reading a word problem.**

Same engine model as [chartlynk](https://github.com/allisonrowell/chartlynk) — a single self-contained `index.html`, no build step, no backend, progress saved in the browser (localStorage), XP + streak + progress bars.

> **Study tool only.** Built from the practice problems Clarke posts *before* class. Per the syllabus, no AI or app of any kind may be used *during* the six graded in-class exercises — that is an Honor Code line. Use this to prepare, then walk in and do it yourself.

## The signature mechanic — the 5-stage Decoder

Every problem is worked as a game with five stages, earning XP at each:

1. **Read** — the word problem, numbers highlighted.
2. **Tag** — assign each number its role (PV, FV, r, t, C, g). *This is the core skill.*
3. **Formula** — pick the right formula from a shortlist; wrong picks explain *why* they're wrong.
4. **Plug in** — drop each tagged value into the formula's slots (with unit-conversion prompts).
5. **Solve** — the arithmetic reveals step by step, ending in the answer + a plain-English "what this means."

## Curriculum

**Track 1 — Time Value of Money** (live): the intuition, the five variables, the **Decoder Method** decision tree, quizzes, and 4 full decoders built from real Exercise-1 problems (deferred payment, annuity, mortgage payment, endowment/perpetuity).

Roadmap (from the same course + Clarke's 2015–2018 practice exams):
2. Capital Budgeting — NPV & IRR (Ch. 5–6)
3. Interest Rates & Bond Pricing (Ch. 8)
4. Stock Valuation / DDM (Ch. 9)
5. Risk, Return & Cost of Capital — WACC (Ch. 10–13)
6. Integrative — EVA / MVA (Ch. 9, 13, 14)

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

FinLYNK is an independent study aid, not affiliated with or endorsed by Georgia Tech or the Scheller College of Business.
