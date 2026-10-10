# Quizzical Club — Team Trivia & Word-Game Night

A light, gentle fork of **Quizzical** for long family sessions: team Jeopardy
boards, a solo practice workbook, and guides for every puzzle type.
Static site, no backend — GitHub Pages ready.

## The three sections

- **🎯 Team Jeopardy** — pick one of five themed sets, split into 1–4 teams,
  and play two boards (round 2 is doubled) plus a final wager. The host reads
  the clue aloud, reveals the answer, and awards points to a team. All content
  comes from the curated book dataset.
- **✏️ Workbook** — practice every puzzle type (homonyms, compound words,
  backwords, heteronyms, letter trivia, initials, hidden words, title swaps,
  geography, general knowledge) as a 10-question test at your chosen
  difficulty, with fuzzy answer checking and per-type best scores saved
  locally.
- **📖 Guides** — how each puzzle type works: rules, a worked example, and
  strategy tips, with one-tap "practice this type".

## Development

```bash
npm install        # or: npm ci
npm run dev        # dev server (forwards --port/--host to vite)
npm test           # vitest: sets validity, workbook pools, guides, matcher, saves
npm run build      # type-check + production build to dist/
npm run preview    # serve the production build locally
npm run e2e        # playwright: all three sections, team scoring, a11y basics
```

## Stack

Vite 8 · React 19 · TypeScript (strict) · Tailwind CSS v4 · React Router 7
(hash routing) · Zustand · Zod · Motion · Vitest · Playwright

## Deployment

Same as the parent project: `base: "./"` and hash routing, so it works at any
GitHub Pages subpath or custom domain. For "GitHub Actions" Pages source use a
standard build-and-deploy workflow; for "Deploy from a branch" run
`npm run publish` and commit the root output (see the parent repo's README).

## Content note

Trivia content is bundled for personal, non-commercial use. No source book
titles or author names appear in the app.
