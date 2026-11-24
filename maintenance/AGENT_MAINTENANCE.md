# GLM / Agent maintenance loop

Use this process for every scheduled or user-requested Math Arena improvement.

1. Read `AGENTS.md`, current README, latest changelog, QA log, known limitations, and recent commit/PR history first.
2. Select one worthwhile improvement; avoid repeating recently completed work. Prefer meaningful user value, reliability, learning outcomes, multiplayer robustness, accessibility, performance, or polish.
3. Create a feature branch. Explain the scope and acceptance criteria in the PR before coding.
4. Implement, test, and perform a regression pass. Record real commands and their results.
5. For every app-facing change, capture **fresh screenshots of the actual build**. Screenshots go into `screenshots/`; include screen/state captions in the PR. If visual evidence cannot be captured, do not mark work complete.
6. Update docs/changelog and `docs/QA_LOG.md`. Increment version/build if appropriate.
7. Build and verify the APK if possible. If a release-worthy build is produced, publish it as a new GitHub Release with the APK, SHA-256, release notes, and install instructions. Never replace prior releases.
8. Check the diff for secrets, accidental unrelated changes, broken paths, and untracked artifacts.
9. Request review via PR. No direct commits to main, no force pushes, no destructive history cleanup.
10. Final report must be accurate and include PR/commit, tests, screenshots, build and release links, and limitations.

## Prompt to GLM

Use the following maintenance prompt (or paste it as the task description):

> Act as Math Arena's autonomous senior Android/game engineer and maintainer. Read the repository instructions and recent audit history first. Pick one substantial improvement with measurable acceptance criteria, implement it on a branch, test it, regression-test relevant behavior, and open a PR. For all app-facing changes, build and capture new screenshots from the real updated build; commit those screenshots under screenshots/ and link them in the PR. Update changelog and docs/QA_LOG.md with exact test results and version/build. Never fabricate screenshots, tests, or release artifacts. Preserve all older versions/releases. Attach any new APK to a new GitHub Release with SHA256. Do not push to main, rewrite history, remove artifacts, or include secrets. If any required evidence is unavailable, mark the task blocked and explain precisely. Finish with an auditable report and links.
