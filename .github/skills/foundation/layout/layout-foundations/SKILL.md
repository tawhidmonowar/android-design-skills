---
name: layout-foundations
description: Use this skill to design or refactor the structural layout of a Jetpack Compose screen. It helps choose the right layout primitives, reduce nesting, enforce clear content hierarchy, and keep layouts stable across phones, tablets, and foldables.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - jetpack compose
  - layout
  - foundation
  - column
  - row
  - box
  - modifier
---

## Objective

Create Compose layouts that are simple, readable, and resilient by using the
smallest correct set of layout primitives.

## Prerequisites

- The project **MUST** use Kotlin.
- New UI work **SHOULD** prefer Jetpack Compose.

## Core workflow

1. Identify the screen's primary regions: top chrome, content, transient state, and primary action.
2. Map each region to the simplest primitive:
   - `Column` for vertical flow
   - `Row` for horizontal flow
   - `Box` for overlap, stacking, or anchored decoration
   - `LazyColumn`, `LazyRow`, or grids for repeated content
3. Remove unnecessary wrappers. A layout **MUST NOT** add an extra container unless it changes measurement, alignment, scrolling, drawing, or semantics.
4. Place `modifier: Modifier = Modifier` on every reusable composable and apply it to the root element.
5. Verify the layout in narrow and wide widths before finalizing the structure.

## Layout rules

- Prefer a shallow hierarchy over deeply nested `Column` and `Row` trees.
- Use `Spacer` for deliberate fixed gaps; use `Arrangement.spacedBy(...)` for repeated rhythm in rows and columns.
- Keep measurement decisions local. Avoid mixing `fillMaxWidth`, `weight`, and hardcoded widths unless the behavior is intentional and verified.
- Prefer alignment APIs over fake spacing. For example, use `horizontalAlignment` or `verticalAlignment` before adding placeholder spacers.
- Reserve `Box` for real overlap or anchoring needs, not as a default container.
- Use `weight` only when sibling elements must share remaining space.

## Validation checklist

- The screen has one obvious root layout strategy.
- The hierarchy is understandable without tracing every modifier.
- Repeated content uses lazy containers instead of manually repeated children.
- The layout stays readable when text grows or shrinks.
- The root composable can be previewed with sample data.
