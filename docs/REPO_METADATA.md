# Recommended GitHub Metadata

These are the recommended descriptions, topics, and profile pin order for the public portfolio launch.

## Repository Descriptions

### Hub

Repository:
`combined-project` or a renamed public hub such as `tower-defense-case-study`

Suggested description:
`Portfolio hub for a tower defense game implemented in Kotlin Android, Godot 4, and Unity 6 with a shared gameplay contract.`

### Android

Repository:
`tower-defense-android`

Suggested description:
`Canonical Kotlin Android Canvas implementation of a tower defense game used as the source of truth for Godot and Unity ports.`

### Godot

Repository:
`tower-defense-godot`

Suggested description:
`Godot 4 port of a Kotlin tower defense game, aligned to the original campaign, progression, and content contract.`

### Unity

Repository:
`tower-defense-unity-port`

Suggested description:
`Unity 6 code-first port of a Kotlin tower defense game with parity-focused campaign, progression, and HUD flow.`

## Suggested Topics

Use a consistent topic family across the three engine repos:

- `tower-defense`
- `game-development`
- `portfolio-project`
- `kotlin`
- `android`
- `godot`
- `godot-4`
- `unity`
- `unity6`
- `csharp`
- `gdscript`
- `gameplay-programming`

Recommended repo-specific emphasis:

- Android: `kotlin`, `android`, `canvas`
- Godot: `godot`, `godot-4`, `gdscript`
- Unity: `unity`, `unity6`, `csharp`

## Suggested Profile Pin Order

1. Docs hub
2. `tower-defense-android`
3. `tower-defense-godot`
4. `tower-defense-unity-port`

## Default Branch Recommendation

- Hub: `main`
- Android: clean public branch, ideally `main` for consistency if you choose to rename from `master`
- Godot: clean public branch, not a work-in-progress feature branch
- Unity: `main`

If renaming Android from `master` to `main` would slow down the release, keep `master` but make sure it is polished and current.
