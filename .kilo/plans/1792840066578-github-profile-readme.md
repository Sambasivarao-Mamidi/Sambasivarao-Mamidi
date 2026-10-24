# Plan: Adapt Aurora Veil profile README

## Goal
Replace `README.md` with the Aurora Veil template adapted for Sambasivarao-Mamidi, including its self-hosted animated SVG hero.

## Source
- Template: `C:\Users\msamb\Downloads\awesome-github-profile-main\templates\09-avant-garde\aurora-veil`
- Asset: `.../assets/avant-garde/aurora-veil.svg`

## Decisions
- Hero asset: `assets/aurora-veil.svg` (copy from gallery, edit in place).
- Name in SVG: `Sambasivarao-Mamidi`
- Role line in SVG: `UI ENGINEER · FRONTEND DEVELOPER`
- Currently: building clean, working products as a UI Engineer / Frontend Developer based in Vishakhapatnam.
- Writing: notes on interfaces, frontend craft, and turning logic into art.
- Epigraph: “Code is poetry written in logic.” — Sambasivarao-Mamidi
- Website: `sambasivarao-mamidi.vercel.app` / `https://sambasivarao-mamidi.vercel.app/`
- Omit Twitter link.
- Remove unused `assets/divider.svg`; keep only `assets/aurora-veil.svg`.

## Affected files
- `README.md`
- `assets/aurora-veil.svg` (new, copied + edited)
- `assets/divider.svg` (remove if unreferenced)

## Tasks
1. Copy gallery SVG to `assets/aurora-veil.svg`.
2. Edit SVG `<text>` elements for name, role line, and optional coordinate/label text.
3. Overwrite `README.md` with Aurora Veil markdown block, filled placeholders and no Twitter link.
4. Remove unused assets.
5. Validate no broken references and review diff.
6. Commit and push to `origin/main`.

## Risks
- SVG filter animation is heavy; keep only one filter-heavy hero.
- Coordinate/label text in SVG may need localization but is optional.
- Asset path must be relative (`./assets/aurora-veil.svg`) for GitHub rendering.

## Validation
- `git diff -- README.md`
- Confirm `assets/aurora-veil.svg` exists and is referenced.
- Confirm commit and push complete.