# Plan: Add clickable links under all profile sections

## Goal
Make every profile section have working clickable links beneath its SVG, including profile links and selected GitHub project links.

## Decisions
- Add Markdown link blocks under:
  - Aurora Veil
  - Open to Work
  - Vinyl Sleeve
- Profile links: Portfolio, LinkedIn, GitHub.
- Project links: use existing repositories:
  - A2Z-DSA-Sheet
  - whatsapp-wrapped
  - Game_Station
  - Portfolio
  - Attendance_Project-main
- Vinyl tracklist links should map to those repositories.
- SVG `<a>` tags remain non-functional on GitHub; Markdown links are the working layer.

## Affected files
- `README.md`

## Tasks
1. Add profile link row under Aurora Veil.
2. Add contact/project links under Open to Work.
3. Add tracklist project links under Vinyl Sleeve, one per track.
4. Validate all URLs are absolute and reachable.
5. Review diff and push.

## Risks
- Long track URLs may wrap; use concise link text.
- Avoid duplicate or broken anchors.

## Validation
- `git diff -- README.md`
- Manual check of all Markdown links.