---
name: android-layout-foundation
description: Use for Android Jetpack Compose layout structure, spacing, alignment, hierarchy, forms, lists, grids, and stateful screen layouts.
---

# Android Layout Foundation

## Use When

Use this skill when creating, reviewing, or refactoring Android UI layouts in Jetpack Compose.

Common tasks:
- Build a new screen layout
- Improve spacing and visual hierarchy
- Fix alignment problems
- Create form, list, grid, or stateful screen layouts
- Make UI cleaner, more responsive, and production-ready

## Core Rules

- Use Jetpack Compose and Material 3.
- Prefer responsive layouts over fixed-size layouts.
- Use `MaterialTheme` colors and typography.
- Use an 8dp spacing rhythm.
- Keep composables small and reusable.
- Hoist state from UI components.
- Avoid business logic inside composables.
- Support loading, empty, error, and success states.
- Check accessibility, touch targets, and readable hierarchy.
- Avoid hardcoded colors, magic numbers, and oversized composables.

## Layout Rules

- Use `Column`, `Row`, `Box`, `LazyColumn`, and `LazyVerticalGrid` intentionally.
- Use `Modifier.fillMaxWidth()` for flexible width.
- Avoid unnecessary fixed `height` and `width`.
- Use `padding` for breathing space.
- Use `Arrangement.spacedBy()` for repeated spacing.
- Use `weight()` carefully and only when flexible distribution is needed.
- Keep screen-level layout separate from reusable components.

## Load Extra References Only When Needed

- Spacing/rhythm: `refs/spacing-rhythm.md`
- Alignment/hierarchy: `refs/alignment-hierarchy.md`
- Forms: `refs/forms.md`
- Lists/grids: `refs/lists-grids.md`
- Stateful screens: `refs/stateful-screens.md`

## Output Checklist

Before final output, verify:

- Layout is responsive.
- Spacing is consistent.
- Typography hierarchy is clear.
- Main CTA is visible.
- Lists use lazy layouts.
- State is hoisted.
- UI handles loading, empty, error, and success states.
- Colors and typography come from `MaterialTheme`.
- Touch targets are comfortable.
- Code is production-ready, not demo-only.