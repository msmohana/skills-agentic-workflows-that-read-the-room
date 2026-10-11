---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site from official GitHub sources.
on:
  workflow_dispatch:
  schedule:
    - cron: '17 9 * * *'

tools:
  edit:
  web-fetch:

network:
  allowed:
    - github.blog
    - github.com
    - awesome-copilot.github.com

safe-outputs:
  create-pull-request:
---

# Update Mona's GitHub info

Update `site/content/github-info.md` with fresh GitHub details that fit Mona's notes and the latest GitHub news.

## Required steps

1. Read `notes/mona-notes.md` to understand Mona's preferences and the site context.
2. Use web-fetch to read external public guidance, including `https://github.blog/latest/`, `https://github.blog/changelog/`, and `https://awesome-copilot.github.com/workflows/`.
3. Read repository guidance or reference files with GitHub repository API tools instead of terminal, CLI, or sandboxed commands.
4. Review the current `site/content/github-info.md` and rewrite it with the latest, relevant GitHub facts.
5. Use safe-outputs with `create-pull-request` so the change can be reviewed as a pull request for Mona.
6. Keep the workflow focused on the GitHub Blog, GitHub Changelog, and Awesome Copilot workflows sources, and ensure the update is easy for Mona to review before merging.

## Review guidance

- Keep the content concise, accurate, and repository-specific.
- Prefer public sources that are relevant to GitHub and developer workflows.
- Update `site/content/github-info.md` and open a pull request for Mona to review after the draft is prepared.
- Validate that the workflow configuration is syntactically correct, but do not compile this agentic workflow markdown.
- Only create or update the markdown workflow file; do not compile it.
