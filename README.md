# 🎮 Tower Defense: Multi-Engine Case Study

This repository serves as a centralized hub for a unified tower defense game implemented across three distinct technology stacks. This project demonstrates high-fidelity game design parity and cross-platform architecture.

- **Kotlin on Android Canvas** (Canonical Implementation)
- **Godot 4** (Engine Port)
- **Unity 6** (Code-First Engine Port)

The core objective of this study is to maintain a consistent game design—including campaign structure, progression models, and content catalogs—while leveraging the unique strengths of each runtime.

---

## 📐 Project Thesis

Kotlin serves as the source of truth for the game's mechanics and data contracts. The Godot and Unity implementations are engineered to achieve strict parity with the Kotlin version in the following areas:

- **Tower & Power Rosters**: Identical stats, abilities, and balancing.
- **Campaign Flow**: 20-level master campaign with synchronized difficulty scaling.
- **Meta-Progression**: Shared achievement logic and skill-tree nodes.
- **User Interface**: Consistent HUD language and menu navigation.

While the user-facing experience is unified, the internal implementation remains native to each engine, showcasing proficiency in Godot's scene-tree architecture, Unity's code-first runtime bootstrap, and Android's low-level Canvas rendering.

---

## 📁 Implementations

| Repository | Stack | Role |
| --- | --- | --- |
| [**tower-defense-android**](https://github.com/rogal01/tower-defense-android) | Kotlin, Android Canvas | Canonical gameplay and data contract |
| [**tower-defense-godot**](https://github.com/rogal01/tower-defense-godot) | GDScript, Godot 4 | Scene-driven engine port |
| [**tower-defense-unity-port**](https://github.com/rogal01/tower-defense-unity-port) | C#, Unity 6 | Code-first runtime bootstrap port |

---

## ⚔️ Shared Gameplay Contract

Every implementation adheres to a rigorous content specification:

- **6 Unique Towers** & **4 Global Powers**
- **5 Diverse Maps** & **8 Dynamic Wave Modifiers**
- **20 Campaign Levels** with unique objectives
- **39 Achievements** & **16 Skill Progression Nodes**

---

## 🚀 Engineering Highlights

- **Multi-Engine Porting**: Successfully translated complex game logic from a Kotlin source into two major engine ecosystems.
- **Content Parity**: Maintained a unified progression and content contract across three heterogeneous codebases.
- **Architecture Adaptability**: Designed engine-specific code that feels native while preserving design consistency.
- **Schema Management**: Implemented robust save-data versioning across SharedPreferences, Godot ConfigFiles, and Unity PlayerPrefs.

---

## 📊 Technical Comparison

| Area | Android | Godot | Unity |
| --- | --- | --- | --- |
| **Runtime Model** | Canvas-driven loop | Scene tree + Autoloads | Code-first bootstrap |
| **Primary Language** | Kotlin | GDScript | C# |
| **Data Ownership** | Centralized in `game` package | `GameData.gd` registry | `TDData.cs` models |
| **Save Model** | SharedPreferences | `ConfigFile` serialization | `PlayerPrefs` serialization |

---

## 📜 Documentation

- [**KOTLIN_PARITY_SPEC.md**](./KOTLIN_PARITY_SPEC.md): Technical specification for exact mechanic parity.
- [**docs/ARCHITECTURE.md**](./docs/ARCHITECTURE.md): Deep dive into the cross-platform design patterns used.

---

## 📜 License
This project is licensed under the MIT License.
