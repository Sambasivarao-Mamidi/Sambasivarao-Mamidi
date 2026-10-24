# Plan: Populate vinyl sleeve with live GitHub repositories

## Goal
Fetch repositories from `https://github.com/Sambasivarao-Mamidi` and use them as the vinyl sleeve tracklist and selected works list.

## Decisions
- Source: live GitHub repository list for `Sambasivarao-Mamidi`.
- Selection: top 5 public repositories by recent activity/stars, excluding forks if possible.
- Update both:
  - `assets/vinyl-sleeve.svg` tracklist rows
  - `README.md` selected works links
- Assign plausible run times to each selected repository.
- Keep profile image links absent unless separately requested.

## Affected files
- `assets/vinyl-sleeve.svg`
- `README.md`

## Tasks
1. Fetch repository list using `gh repo list Sambasivarao-Mamidi --limit 100 --json name,url,description,isFork,pushedAt,stargazerCount`.
2. Select 5 repositories for the tracklist.
3. Update SVG tracklist titles and run times without breaking layout.
4. Update README selected works list with repository names and URLs.
5. Validate no broken links and review diff.
6. Commit and push.

## Risks
- GitHub API/CLI authentication or rate limits.
- Long repository names may overflow the SVG tracklist area.
- Repository list may change; selected set should be deterministic by pushed date.

## Validation
- `git diff -- assets/vinyl-sleeve.svg README.md`
- Confirm all selected repository URLs are valid.