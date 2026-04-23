---
name: list-and-grid-layouts
description: Use this skill to design and implement performant lists and grids in Jetpack Compose. It covers item structure, spacing, keys, sectioning, density, and adaptive grid behavior.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - lazycolumn
  - lazy grid
  - lists
  - grids
  - collection ui
---

## Objective

Present repeated content clearly and efficiently, choosing the right density and
layout for the data.

## Core workflow

1. Identify whether the content is best understood as a list, grid, or grouped sections.
2. Define the information hierarchy inside each item: primary label, secondary metadata, supporting media, and action.
3. Choose a density that matches the task:
   - list for comparison and scanning
   - grid for visual browsing
   - sectioned list for mixed content or categorization
4. Add stable keys and content padding.
5. Validate performance and readability with realistic data counts.

## List and grid rules

- Use lazy containers for repeated content.
- Item layouts **SHOULD** stay structurally consistent across a collection.
- Stable keys **MUST** be used when items can move, update, or animate.
- Grids **SHOULD** preserve a reasonable card width instead of maximizing columns blindly.
- Dividers, badges, and metadata **MUST NOT** overpower the primary content.

## Design guidance

- Use section headers only when they improve scanning or meaning.
- Empty space inside cards should feel intentional, not like missing content.
- Long lists **SHOULD** keep actions lightweight and predictable.
- Skeletons, loading cells, and empty states **SHOULD** match the final layout shape.

## Validation checklist

- Users can scan the collection quickly.
- Item density matches the task and content type.
- The layout behaves well with short, long, and missing content.
- Scrolling remains smooth and state restoration is preserved where needed.
