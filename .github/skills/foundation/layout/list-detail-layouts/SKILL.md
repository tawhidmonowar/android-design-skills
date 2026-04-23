---
name: list-detail-layouts
description: Use this skill to design list-detail and master-detail experiences for Android across phones, tablets, foldables, and large screens. It covers pane behavior, selection, continuity, and adaptive navigation patterns.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - list-detail
  - master-detail
  - adaptive
  - two pane
  - large screen
---

## Objective

Create list-detail experiences that scale naturally from a single-pane phone flow
to wider, productivity-oriented layouts.

## Core workflow

1. Identify the collection, the selected item state, and the detail content requirements.
2. Define the compact behavior first: list to detail navigation.
3. Define medium and expanded behavior:
   - side-by-side panes
   - supporting pane
   - retained selection
4. Ensure selection, back behavior, and deep links remain consistent across widths.
5. Test transitions when resizing between one-pane and two-pane layouts.

## Layout rules

- Compact layouts **SHOULD** prioritize a simple one-pane navigation flow.
- Wide layouts **SHOULD** retain context by keeping the list visible beside details when space allows.
- Selection state **MUST** be visually obvious in multi-pane layouts.
- The detail pane **MUST NOT** appear empty without guidance; provide a placeholder or instructions when needed.
- Pane widths **SHOULD** support reading and scanning, not just split the screen equally by default.

## Design guidance

- Allow the list pane to remain denser and the detail pane to breathe more.
- Keep detail actions close to the detail content, not hidden in the list pane.
- If a supporting pane exists, it **MUST** have a narrowly defined role.
- Avoid modal detail surfaces on wide screens when inline panes provide better continuity.

## Validation checklist

- Compact and expanded layouts feel like the same feature, not separate screens.
- Users can always tell what is selected and what content is being shown.
- Back navigation remains intuitive after resizing or rotation.
- The empty-detail placeholder is informative and visually balanced.
