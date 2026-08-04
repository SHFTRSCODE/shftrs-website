# shftrs website — working rules

Static marketing site for shftrs. Three files, no build step: `index.html` (all markup, CSS and JS inline), `system-visual.html` (embedded system map), `shftrs-logo.svg`.

Nik owns hosting and deployment. This repository is the source; he takes changes from it.

## Git workflow — follow this every session, without being asked

1. **Start on a fresh `main`.** `git checkout main && git pull` before anything else. If `main` has moved since the last session, the working copy is stale and edits will conflict with Nik's.
2. **Never commit to `main`.** Every change goes on a new branch named `sander/<short-description>` — for example `sander/hero-copy`, `sander/pricing-section`.
3. **Commit with a message that explains the change**, not the file touched.
4. **Push the branch** with `git push -u origin <branch>`.
5. **Stop there.** Do not merge, do not open a pull request, do not touch `main`.
6. **End every session by stating the branch name in full**, so Sander can pass it to Nik. This is the handoff — if the branch name isn't stated, the work is invisible.

## Design constraints

The live site uses:

- **Type:** `DM Serif Display` for headings, `DM Sans` for body, loaded from Google Fonts.
- **Palette:** `--paper #F6F1E9`, `--ink #1A1A18`, `--ink-mid #5C5855`, `--ink-faint #9A9690`, `--rule #D8D3CA`, `--accent #B85C38`, `--dark-bg #1A1A18`, `--dark-text #F6F1E9`.

Use the existing CSS custom properties. Do not introduce new colour values or font families without asking.

Note: the Brand Guidelines v1.0 specify Zilla Slab and Plus Jakarta Sans. The live site uses DM Serif Display and DM Sans. This is a real divergence, not an error to correct silently — flag it if it becomes relevant, and let Sander decide which is authoritative.

## Brand rules — non-negotiable

- **`shftrs` is lowercase in running text. `SHFTRS` uppercase is for display and logotype only.** The dropped-vowel spelling is never altered or expanded.
- **Never lead with AI.** shftrs is a methodology company that uses AI to make systems mapping operational — not an AI product. Copy that opens on the technology is wrong.
- **Prefer "systems mapping and analysis"** over "systems thinking" — more concrete, and ownable.
- **Banned words:** innovative, cutting-edge, game-changing, impactful, disrupt, revolutionary. Also avoid "solution" and "fix" when describing what shftrs does to a system — the vocabulary is intervention, leverage points, root causes, structural change, feedback loops.
- **Tone:** quietly confident, precise, warm but not sentimental. Sage archetype with a Magician edge. The register is the most interesting person in the room who isn't trying to be.
- **Positioning line:** shftrs maps why systems behave as they do and identifies where intervention produces structural change.

## Copy discipline

Every sentence must mean something, add value, and be defensible. If a line could appear on any consultancy's website, it is wrong. Do not simplify complexity to make it sellable — the audience is sophisticated and the complexity is the point.

## What not to do

- Do not add a build step, framework, or package manager. It is three static files and that is deliberate.
- Do not add analytics, tracking, or third-party scripts without asking.
- Do not restructure `index.html` wholesale to "clean it up." Make the requested change.
