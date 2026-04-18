# Kotlin Parity Spec

Kotlin is the canonical source of truth for the public portfolio release.

Reference path:
`android-backup/app/src/main/java/com/example/myapp/game`

The Godot and Unity repositories should be treated as ports of that version, not separate design branches.

## Canonical Content

- Towers: `ARROW`, `MAGIC`, `CANNON`, `POISON`, `TESLA`, `ICE`
- Powers: `FIREBALL`, `FREEZE`, `HEAL`, `LIGHTNING`
- Maps: `CLASSIC`, `VALLEY`, `CROSSROADS`, `DESERT`, `SNOW`
- Wave modifiers: `NONE`, `FAST`, `ARMORED`, `REGEN`, `SWARM`, `INVISIBLE`, `RICH`, `BOSS_RALLY`
- Campaign levels: `20`
- Achievements: `39`
- Skill tree nodes: `16`

## Campaign Rules

- Campaign level data does not own a map.
- Map selection is a separate choice from campaign level selection.
- Public release branches should preserve the Kotlin campaign field model:
  - `id`
  - `title`
  - `description`
  - `emoji`
  - `targetWave`
  - `startingGold`
  - `allowedTowers`
  - `allowedPowers`
  - `upgradesEnabled`
  - `enemyHpMult`
  - `enemyDmgMult`
  - `enemySpeedMult`
  - `goldMult`
  - `spawnRateMult`
  - `diamondReward`
  - `hint`

## Skill Tree Contract

Base page nodes:

- `start_gold`
- `base_hp`
- `player_damage`
- `player_speed`
- `player_hp`
- `tower_damage`
- `gold_bonus`
- `diamond_luck`
- `wave_bonus`
- `attack_range`

Prestige page nodes:

- `ice_power`
- `ability_cd`
- `sell_bonus`
- `resist_pierce`
- `wave_modifier`
- `prestige_gold`

## Save Concepts To Preserve

- Diamonds: `diamonds`
- Prestige: `prestige_level`
- Skill levels: `skill_<id>`

The key names do not need to be byte-for-byte identical across every engine, but the public documentation and behavior should preserve the same concepts.

## Required Port Behavior

- Remove or hide all non-Kotlin towers, maps, modifiers, campaign levels, and achievements from the public shipped experience.
- Use a schema version bump in Godot and Unity when incompatible save data would pollute parity mode.
- Count campaign completion against the Kotlin 20-level campaign only.
- Count flawless campaign achievements from no-damage clears, not engine-specific extra scoring systems.
- Keep Kotlin wording and menu intent wherever that wording communicates the gameplay contract more clearly than port-specific terminology.

## Engine-Specific Freedom

The following differences are acceptable and expected:

- scene layout and autoload structure in Godot
- code-first runtime bootstrap and UI construction in Unity
- rendering implementation details, editor setup, and asset pipelines
- engine-native save plumbing as long as the same player-facing progression model is preserved

The following differences should be minimized in the public release:

- extra content that makes the port look like a different game
- divergent campaign structure
- conflicting HUD language
- achievement behavior that changes the meaning of progression
