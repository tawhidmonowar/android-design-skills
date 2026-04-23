---
name: scaffold-and-navigation-chrome
description: Use this skill to structure Android screens with Scaffold, app bars, navigation bars, rails, floating actions, and snackbars. It helps place persistent chrome so content and actions stay organized.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - scaffold
  - top app bar
  - navigation bar
  - navigation rail
  - fab
---

## Objective

Create predictable screen chrome that supports the task instead of competing with
content.

## Core workflow

1. Identify which UI elements are persistent chrome and which are screen content.
2. Decide whether the screen needs top app bar, bottom bar, navigation rail, FAB, snackbar host, or none.
3. Use `Scaffold` when multiple chrome regions must coordinate.
4. Keep the content slot focused on the task-specific body rather than global structure.
5. Verify that persistent chrome does not hide content or duplicate actions already present in the body.

## Chrome rules

- A top app bar **SHOULD** communicate place, context, and navigation.
- A FAB **MUST** represent the single most important screen-level action.
- Bottom navigation and navigation rail **MUST NOT** be used together in the same width class.
- Snackbars **SHOULD** confirm or recover from actions, not replace core screen messaging.
- Screen content **MUST** respect the padding from `Scaffold`.

## Design guidance

- Use simple app bars for focused tasks; use larger app bars only when the screen benefits from stronger identity or scroll behavior.
- Avoid adding both inline CTA buttons and a FAB for the same action.
- Keep chrome density low on content-heavy screens.
- Let navigation components reflect information architecture, not visual preference.

## Validation checklist

- Every persistent chrome element has a clear purpose.
- There is no duplicated primary action.
- The content area remains spacious and readable.
- Navigation chrome adapts appropriately across widths.
