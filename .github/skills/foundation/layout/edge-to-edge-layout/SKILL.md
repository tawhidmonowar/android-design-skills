---
name: edge-to-edge-layout
description: Use this skill to design Compose screens that work correctly with system bars, display cutouts, gesture navigation, and the on-screen keyboard. It focuses on layout and spacing decisions needed for edge-to-edge UI.
license: See LICENSE
metadata:
  author: Android Design Skills
  keywords:
  - android
  - compose
  - edge-to-edge
  - insets
  - ime
  - system bars
  - safe drawing
---

## Objective

Make layouts feel immersive without allowing content or actions to collide with
status bars, navigation bars, or the IME.

## Prerequisites

- Compose screens **MUST** account for window insets.
- The app **SHOULD** prefer official edge-to-edge APIs and inset-aware Material components.

## Core workflow

1. Identify which parts of the UI are decorative and which must remain fully tappable.
2. Determine whether a `Scaffold` can own most inset handling.
3. Apply inset-aware padding only once for a given region.
4. Verify bottom actions, lists, and text inputs against gesture navigation and IME behavior.
5. Check both dark and light system bar legibility.

## Layout rules

- Critical actions **MUST NOT** sit flush against system gesture areas without safe padding.
- Lists **SHOULD** use content padding so first and last items remain accessible.
- Floating buttons, bottom bars, and sticky controls **MUST** remain visible above the navigation bar.
- Text input flows **MUST** remain usable when the keyboard appears.
- Avoid double-applying insets through parent and child containers.

## Recommended patterns

- Use `Scaffold` inner padding for top-level screen structure.
- Use `consumeWindowInsets(...)` when passing `PaddingValues` deeper in the tree.
- Use `safeDrawingPadding()` or specific `WindowInsets` modifiers for custom containers.
- Prefer stable inset handling to ad-hoc fixed padding.

## Validation checklist

- No important UI is clipped by status or navigation bars.
- Keyboard interactions do not hide the focused field or submit action.
- Scrollable content can reach the final item comfortably.
- The screen still looks balanced with immersive content and translucent bars.
