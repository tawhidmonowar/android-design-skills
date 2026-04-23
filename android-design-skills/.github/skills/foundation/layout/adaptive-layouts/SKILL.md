---
name: adaptive-layouts
description: Use this skill to make Android layouts adapt cleanly across compact, medium, and expanded window sizes. It covers phones, tablets, foldables, and multi-window scenarios in Jetpack Compose.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - adaptive ui
  - tablet
  - foldable
  - responsive
  - window size class
---

## Objective

Build screens that preserve structure and usability across different window sizes
instead of merely stretching phone layouts.

## Prerequisites

- Adaptive work **SHOULD** be driven by window size classes or explicit breakpoint logic.
- Layout decisions **MUST** respond to available space, not device names.

## Core workflow

1. Audit the compact layout and separate fixed assumptions from true requirements.
2. Define how the screen behaves in compact, medium, and expanded widths.
3. Promote layout changes progressively:
   - compact: stacked flow
   - medium: increased margins, larger grids, or persistent side content
   - expanded: pane-based or multi-column layouts
4. Ensure reading width remains comfortable. Extra width **SHOULD NOT** become a single endless text line.
5. Test resizing behavior, not just static widths.

## Adaptive rules

- Prefer reflow over scaling. Components **MUST NOT** simply become oversized to fill space.
- Increase margins and column count before increasing individual component height.
- Persistent navigation rail, pane, or supporting content **SHOULD** appear only when it improves task flow.
- Preserve the same core task order across form factors.
- Avoid hardcoded device checks when width and height classes solve the same problem.

## Common strategies

- Single-column to two-column detail layouts
- List to grid transitions for dense content
- Bottom navigation to navigation rail
- Inline supporting pane instead of modal surfaces

## Validation checklist

- The layout remains usable in portrait, landscape, split-screen, and tablet widths.
- Components do not look stretched or stranded in empty space.
- Navigation and primary actions stay easy to find.
- Content order remains logical as panes appear or disappear.
