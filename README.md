# 🎮 My Tower Defense Game (Multi-Engine)

This is a project where I built the same tower defense game using three different things:

- **Kotlin** (on Android) - This was the first one I made and where I keep all the main stats.
- **Godot 4** - A version I built to see how it works in a real game engine.
- **Unity 6** - Another version I made that's mostly just code-driven.

The cool part is that they all have the exact same levels, towers, and gameplay, even though the code is completely different for each.

---

## 🏗️ What I built

I made sure every version of the game has:
- **6 Towers**: Each with their own upgrades and special abilities.
- **4 Powers**: Things like Fireball and Freeze to help you out.
- **20 Levels**: A full campaign that gets harder as you go.
- **Achievements**: Nearly 40 things you can unlock.
- **Save System**: It saves your progress and stars for every level.

---

## 📁 The different versions

| Engine | Language | My Notes |
| --- | --- | --- |
| [**Android**](https://github.com/rogal01/tower-defense-android) | Kotlin | This one is "raw" — no engine, just drawing everything on the screen with code. |
| [**Godot**](https://github.com/rogal01/tower-defense-godot) | GDScript | Used Godot's scene system. It was way faster to build the UI here. |
| [**Unity**](https://github.com/rogal01/tower-defense-unity-port) | C# | I built this one to be almost entirely code-based, not using the editor much. |

---

## 📜 How I kept them synced

I wrote a "master spec" that lists all the tower damage, enemy health, and wave info. Whenever I changed something in the Kotlin version, I updated the Godot and Unity versions to match so the game feels the same everywhere.
