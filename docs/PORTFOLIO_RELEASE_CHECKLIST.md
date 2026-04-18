# Portfolio Release Checklist

Use this checklist before switching the three game repositories to public visibility.

## 1. Branch And Repo Hygiene

- Choose one polished public branch per repository and make it the default branch.
- Do not leave employers landing on WIP feature branches.
- Remove editor caches, machine-local files, and obsolete snapshots from the public branch surface.
- Keep the Android repo positioned as the canonical reference.
- Keep the Godot and Unity repos positioned as ports of that reference.

## 2. README And Landing Page Review

- Confirm each repository README matches the current state of the code.
- Confirm setup instructions are correct and versioned.
- Confirm the Kotlin-first parity story is stated clearly in every repo.
- Add screenshots or short GIFs before switching the repos public.
- Check that links between the hub repo and the three engine repos work.

## 3. Content Parity Review

- Verify the public branch only exposes 6 towers, 4 powers, 5 maps, 8 wave modifiers, 20 campaign levels, 39 achievements, and 16 skill nodes.
- Verify campaign map selection stays separate from campaign level selection.
- Verify save schema resets are enabled where incompatible legacy data exists.
- Verify campaign completion and flawless-clear achievements still match the Kotlin contract.

## 4. Engine-Specific Cleanup

### Android

- Confirm the canonical gameplay data still lives under `app/src/main/java/com/example/myapp/game`.
- Remove build or local-environment noise from the release branch.
- Verify `gradlew.bat assembleDebug` instructions still match the project.

### Godot

- Confirm the shipped branch is the parity-focused version.
- Remove or hide non-canonical content from the public experience.
- Verify `project.godot` opens directly to the intended menu flow.

### Unity

- Keep the public release centered on `Assets/TowerDefensePort`.
- Remove or archive the tracked legacy `My project/` template content from the release branch before publishing.
- Confirm the documented Unity version still opens the project cleanly.

## 5. Media Capture

Capture the same four views for every repository:

- main menu
- gameplay in progress
- HUD and upgrade interaction
- campaign or meta-progression screen

Recommended file naming:

- `media/main-menu.png`
- `media/gameplay.png`
- `media/hud.png`
- `media/meta-progression.png`

## 6. GitHub Publish Steps

- Switch repository visibility from private to public only after the cleanup pass is complete.
- Set the repo descriptions and topics listed in `docs/REPO_METADATA.md`.
- Pin the hub repo first, then Android, Godot, and Unity on the GitHub profile.
- Make sure the hub README is the best first click for employers.

## 7. Final Sanity Check

- Open each repo as if you were a recruiter seeing it for the first time.
- Check the first screen, first paragraph, and first screenshot.
- If something looks like local dev clutter instead of a finished case study, clean it before publishing.
