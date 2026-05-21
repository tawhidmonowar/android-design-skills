## Android Design Skills

[![Agent Skills](https://img.shields.io/badge/Agent-Skills-blue?style=flat&logo=github)](https://agentskills.io)
[![Android](https://img.shields.io/badge/Android-Design-green?style=flat&logo=android)](https://developer.android.com)

`android-design-skills` is a focused Android agent-skill pack for UI design and
layout work in Jetpack Compose.

The repo intentionally combines two ideas from your reference projects:

- `awesome-android-agent-skills-referance`: use a clean, discoverable `.github/skills/...` folder structure
- `skills-main-referance`: use more formal, official-style `SKILL.md` files with frontmatter, prerequisites, objectives, and explicit workflows

## Repository structure

```text
android-design-skills/
├── Agent.md
├── LICENSE
├── README.md
└── .github/
    └── skills/
        └── foundation/
            └── layout/
                ├── adaptive-layouts/
                │   └── SKILL.md
                ├── alignment-and-hierarchy/
                │   └── SKILL.md
                ├── edge-to-edge-layout/
                │   └── SKILL.md
                ├── form-layouts/
                │   └── SKILL.md
                ├── layout-foundations/
                │   └── SKILL.md
                ├── list-and-grid-layouts/
                │   └── SKILL.md
                ├── list-detail-layouts/
                │   └── SKILL.md
                ├── scaffold-and-navigation-chrome/
                │   └── SKILL.md
                ├── spacing-and-rhythm/
                │   └── SKILL.md
                └── stateful-screen-layouts/
                    └── SKILL.md
```

## Available skills

All 10 skills currently live under `.github/skills/foundation/layout/`.

1. **[Layout Foundations](.github/skills/foundation/layout/layout-foundations/SKILL.md)**: Choose the right Compose layout primitives and reduce unnecessary nesting.
2. **[Spacing and Rhythm](.github/skills/foundation/layout/spacing-and-rhythm/SKILL.md)**: Establish consistent spacing tokens and visual rhythm.
3. **[Alignment and Hierarchy](.github/skills/foundation/layout/alignment-and-hierarchy/SKILL.md)**: Improve scanability, alignment, and emphasis.
4. **[Adaptive Layouts](.github/skills/foundation/layout/adaptive-layouts/SKILL.md)**: Design for compact, medium, and expanded window sizes.
5. **[Edge-to-Edge Layout](.github/skills/foundation/layout/edge-to-edge-layout/SKILL.md)**: Handle insets, system bars, and IME-safe layouts.
6. **[Scaffold and Navigation Chrome](.github/skills/foundation/layout/scaffold-and-navigation-chrome/SKILL.md)**: Structure top bars, navigation, FABs, and snackbars.
7. **[List and Grid Layouts](.github/skills/foundation/layout/list-and-grid-layouts/SKILL.md)**: Build clear, performant repeated-content layouts.
8. **[Form Layouts](.github/skills/foundation/layout/form-layouts/SKILL.md)**: Organize fields, validation, and submit actions.
9. **[Stateful Screen Layouts](.github/skills/foundation/layout/stateful-screen-layouts/SKILL.md)**: Design loading, empty, error, and offline states.
10. **[List-Detail Layouts](.github/skills/foundation/layout/list-detail-layouts/SKILL.md)**: Scale master-detail flows from phones to large screens.

## Skill authoring conventions

Each skill follows a shared structure inspired by the official Android skills
repository:

- YAML frontmatter with `name`, `description`, `license`, and `metadata`
- a clear `Objective`
- optional `Prerequisites`
- a practical `Core workflow`
- explicit rules and validation guidance

This keeps the pack easy for agents to parse while still being readable for
humans.

## Installation

Copy `.github/skills/` and `Agent.md` into the root of the Android project where
you want your AI agent to discover these skills.

Example:

```text
my-android-project/
├── Agent.md
├── .github/
│   └── skills/
│       └── foundation/
│           └── layout/
│               └── ...
└── app/
```

## Usage

Ask your agent to apply one of the skills directly, for example:

- `Read .github/skills/foundation/layout/adaptive-layouts/SKILL.md and refactor this screen for tablets.`
- `Use the form-layouts skill to clean up this checkout form.`
- `Apply the edge-to-edge-layout skill to this Compose screen.`






skills/
├── android-layout-foundation/
├── android-material3-design/
├── android-compose-components/
├── android-compose-performance/
├── android-adaptive-ui/
├── android-accessibility/
├── android-navigation-scaffold/
├── android-screen-patterns/
├── android-ui-review/
└── android-production-quality/
android-animation-motion/
android-theme-system/
android-design-system/
android-form-validation/
android-permission-ui/
android-empty-error-loading-states/
android-play-store-screenshot-ui/
android-wear-tv-large-screen/
android-compose-testing-ui/