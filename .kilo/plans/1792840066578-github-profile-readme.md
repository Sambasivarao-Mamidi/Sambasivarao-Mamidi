# Plan: Replace GitHub profile README

## Goal
Replace `README.md` with a clean, neat, unique, creative profile README using a dark neon theme and selected sections.

## Decisions
- Theme: Dark neon (cyan/violet gradients, terminal accents, dark background).
- Sections: Hero + about, Tech stack, Contact/socials, Fun terminal footer.
- Exclude: Featured projects table and GitHub stats cards.
- Hero is text-only (no image assets), using centered markdown/HTML heading and badges.
- Creative accent: Terminal prompt style (`$ whoami`, `$ cat about.txt`, `$ exit 0`).
- Tech stack badges: existing skills only (HTML5, CSS3, JavaScript, React, Node.js, MongoDB, Python, Java, Git, Figma, VS Code), grouped by category.
- Contact/socials: Portfolio, LinkedIn, GitHub.
- Assets directory can be removed if no remaining references.
- Rollout: Commit and push to `origin/main`.

## Affected files
- `README.md` (overwrite)
- `assets/hero-banner.svg`, `assets/divider.svg` (remove if unreferenced)
- Legacy GIF/PNG assets already removed.

## Implementation tasks
1. Overwrite `README.md` with:
   - Centered text-only hero: name, role, location, short tagline.
   - `whoami` terminal bio section.
   - Tech stack badges grouped as Frontend, Backend & Database, Tools.
   - Contact/social badges.
   - Terminal footer with `$ exit 0`.
2. Remove unused assets if no references remain.
3. Review diff for accidental binary or asset changes.

## Failure modes
- External badge service outage: shields.io badges may not render; use standard badge URLs only.
- Relative asset paths must not point to removed files.
- Push may fail due to auth/network; retry or report status.

## Validation
- `git diff -- README.md`
- Confirm no missing asset references.
- Confirm commit and push complete.