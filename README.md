# Math Arena — Grade 10

**Math Arena** is a competitive Grade-10 mathematics Android learning game. The upstream project currently includes offline game modes, textbook-based question content, adaptive practice, and online multiplayer/server components.

> Repository bootstrap: this repository is being prepared for a full source import. The original project archive is not yet uploaded here. APK binaries and other non-text artifacts require an upload method that supports binary files; they are not silently omitted or represented as uploaded.

## Repository operating rules

- **Auditable changes:** every update must be committed; no force-pushes or history rewriting. Commit messages must explain what changed.
- **Visual proof:** any change affecting app screens, gameplay, layout, interaction, graphics, or user-facing behavior must include fresh screenshots under `screenshots/` in the same PR. Screenshots must be from the actual build, not mockups.
- **QA:** document test commands, outcomes, known issues, and build identifier in `docs/QA_LOG.md` for each change.
- **Build identity:** bump the version/build metadata when producing a new release; keep earlier releases/artifacts available.
- **Release integrity:** attach APKs as GitHub Release assets, not committed binaries, and include SHA-256 checksums and install notes.
- **Do not commit secrets:** signing keys, passwords, tokens, API keys, private data, or developer credentials must never enter the repository. If any are found, stop and report; do not copy them.

## Mobile-first repository management

Use GitHub's mobile app or browser to review commits, issues, pull requests, Actions runs, release notes, and files. GitHub Actions provides automated checks. For actual code editing/building beyond the browser's editor, use a cloud coding environment such as GitHub Codespaces (if enabled on the account) or an agent that works through pull requests.

## Required visual evidence for app changes

Put current, clearly labeled screenshots in `screenshots/` (example: `screenshots/vX.Y.Z-home.png`). Each PR should include a short caption or notes describing what each screenshot proves. The screenshot-check workflow blocks app-facing PRs that do not include fresh screenshot files.

## Structure (target)

- `app/` — game UI and assets
- `android/` — Android wrapper/native files
- `server/` — multiplayer/backend
- `content/` — curriculum and validated question-bank pipeline
- `scripts/` — build, test, QA tools
- `docs/` — architecture, changelog, test and QA reports
- `screenshots/` — fresh, build-specific visual evidence
- `release-assets/` — source project release artifacts (avoid committing large binaries)
- `maintenance/` — GLM/agent prompts and maintenance procedures

## Start here

- [Agent instructions](AGENTS.md)
- [Maintenance workflow](maintenance/AGENT_MAINTENANCE.md)
- [Audit / QA log](docs/QA_LOG.md)
- [Screenshot policy](docs/SCREENSHOT_POLICY.md)
