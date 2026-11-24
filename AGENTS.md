# Agent instructions — Math Arena

You are working in the Math Arena Grade-10 Android game repository. Make high-quality, substantive, tested improvements. Do not settle for cosmetic tweaks or generic template output.

## Before changing anything
1. Inspect the existing implementation, repository history, issues, and docs.
2. Identify the actual current version/build and relevant limitations.
3. Make a plan, then implement it. Preserve existing working behavior unless a change is intentional.
4. Avoid leaking secrets. Search your intended changes and git diff for credentials, signing keys, private URLs, and tokens. If found, STOP and report.

## Every task must be auditable
- Work on a feature branch and submit a PR; do not push directly to main.
- Keep commits focused, descriptive, and small enough to review.
- PR description: goal, files/areas changed, design decisions, tests run (with exact results), known limitations, and rollback notes.
- Update docs/changelog and `docs/QA_LOG.md` with date, version/build, summary, tests, result, and known issues.
- Never rewrite or delete previous release history or prior build artifacts without explicit permission.

## Screenshots are mandatory for user-facing changes
For every change touching UI, layout, visuals, navigation, gameplay interaction, animations, or user-visible states:
1. Build and launch the actual app version.
2. Capture fresh screenshots from that exact build/device or emulator.
3. Save them in `screenshots/` with version/build + screen/state in filenames.
4. Add screenshots to the PR and explain what each demonstrates.
5. If screenshot capture is impossible, mark the PR BLOCKED and explain why; do not fake, draw, reuse, or claim screenshots are new.
The screenshot gate checks that at least one screenshot file is added or modified in the PR.

## QA expectations
- Run relevant tests, plus regression checks for existing functionality.
- Test both offline and online paths when changes affect networking.
- Test on multiple screen sizes/orientations if UI is affected.
- Record actual test output. Never say tests passed unless run.
- Do not use mocks as a substitute for end-to-end checks without clearly labeling them.
- Add/update tests when bugs are fixed.
- Build APK; verify installable artifact; attach it to a GitHub Release with SHA256, changelog, and install notes. Preserve older releases.

## Versioning and delivery
- Update app version/build metadata when releasing.
- Every release must have a unique tag and immutable version number.
- Keep old releases available; do not overwrite old APKs.
- Release notes should clearly list new features, fixes, test results, screenshots, and known limitations.

## Output / final PR report
At the end, report: summary, changed files, screenshots (links or filenames), tests with pass/fail/skipped status, build artifact/release link, risks/limitations, and exact commit/PR references.
