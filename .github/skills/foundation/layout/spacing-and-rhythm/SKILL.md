---
name: spacing-and-rhythm
description: Use this skill to establish consistent spacing in Android UI with Jetpack Compose. It guides padding, gaps, grouping, and vertical rhythm so screens feel intentional instead of crowded or randomly spaced.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - jetpack compose
  - spacing
  - rhythm
  - padding
  - whitespace
  - design system
---

## Objective

Create a predictable spacing system that improves readability, scannability, and
visual consistency across the app.

## Prerequisites

- The screen **SHOULD** use a shared spacing scale from the design system when one exists.
- If no spacing scale exists, create a small, reusable scale before inventing one-off values.

## Core workflow

1. Identify the screen's spacing tokens or infer a compact scale such as `4dp`, `8dp`, `12dp`, `16dp`, `24dp`, and `32dp`.
2. Group content by meaning: screen padding, section spacing, component internal padding, and micro-gaps between labels or icons.
3. Replace arbitrary values with the nearest shared token.
4. Ensure larger conceptual breaks use larger spacing than intra-component gaps.
5. Re-check the screen for crowding, accidental tangencies, and uneven vertical rhythm.

## Spacing rules

- Outer screen padding **SHOULD** be larger than internal component padding.
- Related items **MUST** sit closer together than unrelated groups.
- Prefer one spacing source per container. Avoid combining `Spacer`, `padding`, and `Arrangement.spacedBy(...)` to solve the same gap.
- Use larger spacing to separate sections, not to patch weak hierarchy.
- Hardcoded one-off spacing values **SHOULD NOT** be introduced unless tied to a documented visual requirement.

## Recommended token usage

- `4dp` to `8dp`: icon-label and micro-spacing
- `12dp` to `16dp`: component internal spacing
- `16dp` to `24dp`: card padding and section gaps
- `24dp` to `32dp`: major screen sections and hero spacing

## Validation checklist

- Similar components use the same spacing rules.
- Section breaks are visually obvious without feeling empty.
- The layout still looks balanced with long text, large font, and RTL.
- Padding values can be centralized into a design token object if needed.
