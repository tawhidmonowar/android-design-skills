---
name: alignment-and-hierarchy
description: Use this skill to improve visual hierarchy and alignment in Android UI. It helps arrange text, actions, and media so users can scan quickly and understand what matters first.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - alignment
  - hierarchy
  - typography
  - scanning
  - balance
---

## Objective

Make the importance of each element obvious by aligning content consistently and
building strong visual hierarchy.

## Core workflow

1. Identify primary, secondary, and supporting information on the screen.
2. Choose one dominant alignment model for each section: start-aligned, center-aligned, or distributed.
3. Align related text baselines and component edges before adjusting spacing.
4. Emphasize importance with position, size, weight, and contrast in that order.
5. Review the screen from top to bottom and confirm the eye lands on the intended focal point first.

## Hierarchy rules

- Start alignment is the default for content-heavy Android screens.
- Center alignment **SHOULD** be reserved for simple, celebratory, or empty-state layouts.
- One section **SHOULD** have a clear primary action. Avoid presenting multiple equally loud CTAs.
- Supporting metadata **MUST NOT** compete visually with title or primary value content.
- Icons and images **SHOULD** support comprehension, not replace labels when labels are needed.

## Alignment rules

- Keep left and right edges intentional across cards, lists, and top-level sections.
- Align text to text and actions to actions. Do not let controls float independently without purpose.
- Use baseline alignment where text sizes differ in the same row.
- Keep action placement predictable across repeated items.

## Validation checklist

- A user can identify the title, supporting copy, and primary action in under a second.
- Repeated items align consistently.
- The layout still feels balanced in both short and long content cases.
- No element appears visually important by accident.
