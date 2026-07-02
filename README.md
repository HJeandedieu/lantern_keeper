<div align="center">

# The Last Lantern Keeper

### *A Light in the Dark*

**A 2D story-driven adventure platformer about being the last source of light in a world consumed by darkness.**

[![Unity](https://img.shields.io/badge/Unity-6-black?style=for-the-badge&logo=unity&logoColor=white)](https://unity.com/)
[![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)](https://learn.microsoft.com/en-us/dotnet/csharp/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](./LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Development-27DBDB?style=for-the-badge)](#-development-roadmap)

</div>

<br>

## Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Gameplay](#-gameplay)
- [Screenshots](#-screenshots)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Development Roadmap](#-development-roadmap)
- [Team](#-team)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgements](#-acknowledgements)

<br>

## Overview

**The Last Lantern Keeper** is a 2D story-driven adventure platformer built in **Unity 6**. A mysterious darkness has extinguished the ancient lighthouses that once protected the kingdom, allowing shadow creatures to spread across the land.

You play as a young adventurer whose name is chosen by the player, the last surviving Lantern Keeper. Armed with a magical lantern—your only tool, your only weapon, and your only true protection—you must journey across the kingdom, relight the ancient lighthouses, and restore light to a world that has long been consumed by darkness.

The game combines exploration, environmental puzzle-solving, platforming, and a signature light-vs-shadow survival mechanic into a single, cohesive experience built around one idea: **light is life.**

<br>

## Features

- [x] Story-driven adventure across a slowly-restoring kingdom
- [x] Light-based puzzle solving using the lantern's evolving abilities
- [ ] Living Shadow enemy mechanic tied to lantern energy
- [x] Precision 2D platforming
- [ ] Progressive lantern abilities (Light Orbs, Plant Platforms, Reflection, and more)
- [ ] Ancient lighthouse restoration and world-state progression
- [ ] Stylized 2D environments with a signature light/dark color palette
- [ ] Persistent save system
- [ ] Atmospheric, state-reactive soundtrack

> Checklist reflects current implementation status and will be updated as development progresses.

<br>

## Gameplay

Each region of the game follows the same core loop: **explore → solve → survive → restore.**

The player enters a new region, platforms and explores its environment, solves environmental puzzles using the lantern, and either fights or evades shadow creatures along the way. Reaching the region's ancient lighthouse and overcoming its final challenge relights it — restoring light to that part of the world and unlocking a brand-new lantern ability that carries forward into every region after it.

<details>
<summary><strong>Signature Mechanic — The Living Shadow</strong></summary>
<br>

The lantern has limited energy that depletes over time and with use. As it weakens, the world grows darker, the music grows tense, and shadow creatures grow bolder. If the lantern's energy hits zero, it extinguishes — and the player's own shadow separates from the ground and comes alive, hunting them until the lantern is reignited or another light source is found.

This turns lantern management into the game's core tension: light is never just visibility — it's survival.

</details>

<br>

## Screenshots

> **Coming Soon**
> Gameplay screenshots and trailers will be added during development.

<br>

## Technology Stack

| Technology | Purpose |
|---|---|
| **Unity 6** | Core game engine |
| **C#** | Gameplay programming and systems |
| **Git** | Version control |
| **GitHub** | Repository hosting and collaboration |
| **Unity URP (2D)** | Rendering pipeline and dynamic 2D lighting |
| **Unity Tilemaps** | Level construction and collision layout |
| **JSON Save System** | Player progress and settings persistence |

<br>

## Project Structure


````
Assets/
│
├── Animations/
├── Art/
├── Audio/
│   ├── Music/
│   └── SFX/
├── Data/                  # ScriptableObjects (lantern tuning, ability configs, enemy stats)
├── Materials/
├── Prefabs/
│   ├── Player/
│   ├── Enemies/
│   ├── Environment/
│   └── UI/
├── Resources/              # Runtime-loaded assets only — not a general dumping ground
├── Scenes/
├── Scripts/
│   ├── Core/               # Core.asmdef — engine-agnostic systems, shared utilities
│   ├── Gameplay/           # Gameplay.asmdef
│   │   ├── Player/
│   │   ├── Enemies/
│   │   ├── Lantern/
│   │   └── Managers/
│   ├── UI/                 # UI.asmdef
│   └── Utilities/
├── Shaders/
├── Sprites/
│   ├── Player/
│   ├── Enemies/
│   ├── Environment/
│   └── UI/
└── UI/
````

> **Notes:**
> - `Data/` holds ScriptableObject assets (e.g. lantern energy/drain values, per-ability configs) so gameplay tuning never requires a code change.
> - `Resources/` is reserved strictly for assets loaded at runtime via `Resources.Load` — everything else lives in its normal folder to avoid bloating build size.
> - `Scripts/` is split into three assembly definitions (`Core`, `Gameplay`, `UI`) to keep compile times fast as the codebase grows and to enforce clean dependency boundaries between systems.
> - Binary assets (`Art/`, `Sprites/`, `Audio/`) are tracked with **Git LFS** to keep repository history lean.

<br>

## Getting Started

### Prerequisites

- [Unity Hub](https://unity.com/download) with **Unity 6** (2D URP) installed
- [Git](https://git-scm.com/) installed locally
- A code editor with C# support (Visual Studio, VS Code, or Rider recommended)

### Clone the Repository

```bash
git clone https://github.com/Hjeandedieu/the-last-lantern-keeper.git
cd the-last-lantern-keeper
```

### Open with Unity 6

1. Open **Unity Hub**
2. Click **Add** → select the cloned project folder
3. Ensure the project is opened with **Unity 6**
4. Let Unity import all assets and packages

### Run the Project

1. In the Unity Editor, open `Assets/Scenes/` and load the main scene
2. Press **Play** to run the game in the Editor

<br>

## Development Roadmap

Progress against the project's 8-week implementation plan:

- [x] Project Planning & Documentation
- [ ] Environment Setup, Git Workflow & Learning Phase
- [ ] Player Controller & Core Movement
- [ ] Lantern System (Energy, UI, Lighting)
- [ ] Living Shadow Mechanic
- [ ] Enemy AI
- [ ] Chapter 1 — The Fading Village
- [ ] Chapter 2 — Whispering Woods
- [ ] Audio & Visual Polish Pass
- [ ] Menus, Save System & Game State Flow
- [ ] Bug Fixing & Optimization
- [ ] Final Build & Presentation

<br>

## Team

| Name | Role |
|---|---|
| **Developer 1** | Gameplay & Systems Programming |
| **Developer 2** | Level Design & Player Experience |

<br>

## Contributing

This is currently a closed student/capstone project, but the workflow below is used for all internal collaboration and will apply to any future external contributions:

1. **Fork** the repository
2. **Create a branch** for your feature or fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Commit** your changes with clear, descriptive messages:
   ```bash
   git commit -m "Add: brief description of the change"
   ```
4. **Push** your branch and **submit a Pull Request** against `dev`, describing what changed and why

Please keep pull requests focused and scoped to a single feature or fix where possible.

<br>

## License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

<br>

## Acknowledgements

- **Unity Technologies** — for the engine and tools powering this project
- **Open-source asset creators** — whose work supports rapid prototyping and learning
- **Contributors** — everyone who helps improve this project
- **The game development community** — for the tutorials, forums, and shared knowledge that made this project possible

<br>

<div align="center">

*"Light is life."*

</div>