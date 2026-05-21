# AGENTS Guidelines for This Repository

This repository is an Android design skill pack, not an application codebase.
When an AI agent works in this repo, it should preserve the repository's purpose:
author reusable Android UI and layout skills that are easy for both humans and
agents to consume.

## 1. Repository intent

- This repo packages Android design guidance as modular `SKILL.md` files.
- Skills **MUST** live in `.github/skills/...` so agent tooling can discover them.
- Folder structure **SHOULD** stay clean and category-first, similar to
  `awesome-android-agent-skills-referance`.
- Skill content **SHOULD** follow the more formal style seen in
  `skills-main-referance`.

## 2. Skill file requirements

Every new skill **MUST** include:

- YAML frontmatter
- `name`
- `description`
- `license`
- `metadata.author`
- `metadata.keywords`

Every new skill **SHOULD** include:

- `Objective`
- `Prerequisites` when needed
- `Core workflow`
- explicit rules or constraints
- a short validation checklist

## 3. Content guidelines

- Prefer Jetpack Compose for all new UI guidance.
- Align with official Android guidance and Material 3 patterns where applicable.
- Use imperative, agent-friendly instructions such as `MUST`, `SHOULD`, and
  clear numbered workflows.
- Keep each skill focused on one problem domain.
- Avoid vague motivational text or generic filler.
- Do not reference files that do not exist.

## 4. Scope of this pack

Current skill taxonomy:

- `foundation/layout/`

Current focus:

- screen structure
- spacing and hierarchy
- adaptive layouts
- edge-to-edge layout
- scaffold and navigation chrome
- forms, lists, grids, and stateful screen layouts

## 5. Maintenance rules

- Update `README.md` whenever a new category or skill is added.
- Keep skill names filesystem-friendly and kebab-cased.
- Prefer stable terminology across skills so agents can route tasks correctly.
- Preserve compatibility with common agent discovery paths based on `.github/skills`.

## 6. Authoring principle

If a skill is inspired by official Android documentation, translate that guidance
into concise, reusable instructions for agents rather than copying long prose.

When in doubt, optimize for:

1. clear structure
2. practical steps
3. Android-specific correctness
4. easy discoverability
