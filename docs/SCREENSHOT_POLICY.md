# Screenshot policy

Screenshots are visual QA evidence and must be fresh for each app-facing PR.

## Requirements
- Capture screenshots from the real app, running the updated code on a device/emulator.
- Use descriptive filenames such as `screenshots/v2.2.0-home.png`, `screenshots/v2.2.0-duel-results.png`.
- Screenshots must show the actual UI and state being tested; don't fabricate, recreate, AI-generate, or recycle old images as fresh evidence.
- Include a PR caption describing screen, device/emulator, build, and what changed.
- When capture cannot be performed, mark screenshot QA as blocked and explain the environment limitation.

## Gate
The screenshot check requires an added/changed PNG, JPEG, or WebP in `screenshots/` for any PR that changes app-facing files in `app/` or `android/`. Documentation-only PRs may omit screenshots.
